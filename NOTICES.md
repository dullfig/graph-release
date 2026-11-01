# Third-party notices

graph's installer includes software made by others. Each part stays under its own licence, listed here. graph's
own code is not open source; see [TERMS.md](TERMS.md).

This list describes graph 0.2.101. It is worked out from what the build actually bundles (production code
only; build and test tools are not shipped).

## Anthropic software (proprietary)

graph's agents run on Anthropic's Claude Agent SDK. Two parts of it are shipped, unmodified:

| Component | Version | Shipped as |
|---|---|---|
| Claude Agent SDK (`@anthropic-ai/claude-agent-sdk`) | 0.3.283 | its JavaScript, bundled into graph's server file |
| Claude Agent SDK native program (`claude.exe`, from `@anthropic-ai/claude-agent-sdk-win32-x64`) | 0.3.283 | `claude\claude.exe`, as published |

> © Anthropic PBC. All rights reserved. Use is subject to the Legal Agreements outlined here:
> https://code.claude.com/docs/en/legal-and-compliance.

These components are not covered by graph's terms and are not licensed to you by graph's author. Your use of
them is subject to Anthropic's agreements and to the terms of the Anthropic account you sign in with.

## Node.js runtime

| Component | Version | Licence |
|---|---|---|
| Node.js (`runtime\node.exe`, the official Windows x64 build) | 24.16.0 | MIT, plus the licences of the libraries built into Node.js |

Node.js is © OpenJS Foundation and Node.js contributors. Its full licence, including the notices of the
libraries built into it (V8, libuv, OpenSSL, ICU, zlib and others), is the `LICENSE` file in the Node.js
distribution: https://github.com/nodejs/node/blob/v24.16.0/LICENSE

## npm packages bundled into graph

Counts: **88 MIT**, **2 ISC**, **1 BSD-3-Clause**, **1 MPL-2.0** (92 packages), plus the 2 Anthropic components
above.

### MIT

**In graph's server** (`app\server.mjs` and the files beside it):
@hono/node-server 2.1.1, @modelcontextprotocol/sdk 1.30.1, ajv 8.20.0, ajv-formats 3.0.1, content-type 1.0.5,
fast-deep-equal 3.1.3, hono 4.13.9, json-schema-traverse 1.0.0, web-tree-sitter 0.27.0 (including
`web-tree-sitter.wasm`), ws 8.22.0, zod 4.6.5.

**Tree-sitter grammars** (`app\grammars\`): @vscode/tree-sitter-wasm 0.3.1 (© Microsoft Corporation), which
packages the tree-sitter TypeScript, Rust and Python grammars (MIT, © their tree-sitter authors).

**In graph's window** (`app\web\`):
bail 2.0.2, ccount 2.0.1, comma-separated-tokens 2.0.3, decode-named-character-reference 1.3.0, devlop 1.1.0,
escape-string-regexp 5.0.0, estree-util-is-identifier-name 3.0.0, extend 3.0.2, hast-util-to-jsx-runtime 2.3.6,
hast-util-whitespace 3.0.0, html-url-attributes 3.0.1, inline-style-parser 0.2.7, is-plain-obj 4.1.0,
longest-streak 3.1.0, markdown-table 3.0.4, mdast-util-find-and-replace 3.0.3, mdast-util-from-markdown 2.1.0,
mdast-util-gfm 3.1.0, mdast-util-gfm-autolink-literal 2.0.1, mdast-util-gfm-footnote 2.1.0,
mdast-util-gfm-strikethrough 2.0.1, mdast-util-gfm-table 2.0.0, mdast-util-gfm-task-list-item 2.0.0,
mdast-util-phrasing 4.1.0, mdast-util-to-hast 13.2.1, mdast-util-to-markdown 2.2.0, mdast-util-to-string 4.0.0,
micromark 4.0.3, micromark-core-commonmark 2.0.4, micromark-extension-gfm 3.0.0,
micromark-extension-gfm-autolink-literal 2.1.0, micromark-extension-gfm-footnote 2.1.0,
micromark-extension-gfm-strikethrough 2.1.0, micromark-extension-gfm-table 2.1.2,
micromark-extension-gfm-tagfilter 2.0.0, micromark-extension-gfm-task-list-item 2.1.0,
micromark-factory-destination 2.0.1, micromark-factory-label 2.0.1, micromark-factory-space 2.1.0,
micromark-factory-title 2.0.1, micromark-factory-whitespace 2.0.1, micromark-util-character 2.1.1,
micromark-util-chunked 2.0.1, micromark-util-classify-character 2.0.1, micromark-util-combine-extensions 2.0.1,
micromark-util-decode-numeric-character-reference 2.0.2, micromark-util-decode-string 2.0.1,
micromark-util-edit-map 1.0.0, micromark-util-encode 2.0.1, micromark-util-html-tag-name 2.0.1,
micromark-util-normalize-identifier 2.0.1, micromark-util-resolve-all 2.0.1, micromark-util-sanitize-uri 2.0.1,
micromark-util-subtokenize 2.1.0, property-information 7.2.0, react 19.3.0, react-dom 19.3.0,
react-markdown 10.1.0, remark-gfm 4.0.1, remark-parse 11.0.0, remark-rehype 11.1.2, scheduler 0.28.0,
space-separated-tokens 2.0.2, style-to-js 1.1.21, style-to-object 1.0.14, trim-lines 3.0.1, trough 2.2.0,
unified 11.0.5, unist-util-is 6.0.1, unist-util-position 5.0.0, unist-util-stringify-position 4.0.0,
unist-util-visit 5.1.0, unist-util-visit-parents 6.0.2, vfile 6.0.3, vfile-message 4.0.3, zwitch 2.0.4.

### ISC

zod-to-json-schema 3.25.2 (server), @ungap/structured-clone 1.4.0 (window).

### BSD-3-Clause

fast-uri 3.1.8 (server).

### MPL-2.0

@terrastruct/d2 0.1.33 (window), the D2 diagram renderer, © Terrastruct, Inc. It is shipped unmodified. Its
source code is available at https://github.com/terrastruct/d2 and in the npm package `@terrastruct/d2`. The
Mozilla Public License 2.0 is at https://mozilla.org/MPL/2.0/.

## Full licence texts

MIT, ISC and BSD-3-Clause require their copyright notice and licence text to travel with every copy. Each
package's own `LICENSE` file is the authoritative text and copyright line. *[Draft note: the installer does not
ship these texts yet; see the recommendation below. Once it does, this section points to the file.]*

---

## For the operator (remove before publishing)

**What was checked.** Bundled packages were derived from the build itself: esbuild's metafile for the server and
launcher (`src/main.ts`, `src/launcher/main.ts`, as in `installer/bundle.mjs`) and the modules Vite actually
transforms for the window (`web/vite.config.ts`), then each package's `package.json` `license` field and
licence files. `org-tree-view` is graph's own code (`tree/`). `@xyflow/react` (MIT) and `elkjs`
(EPL-2.0 OR GPL-3.0-or-later) are listed in `package.json` dependencies but nothing shipped imports them; they
are not in the bundles. If they ever come back into use, elkjs needs its own look (EPL/GPL). Git for Windows and
the GitHub CLI are not shipped: the installer has winget download them from their publishers.

**Needs the full text shipped:** all 88 MIT, 2 ISC and 1 BSD-3-Clause packages (copyright notice plus licence
text), Node.js's `LICENSE` (MIT plus its bundled libraries' notices), and an MPL-2.0 notice for D2. Today
`installer/package.mjs` copies only `node.exe` from the Node zip, and the bundles drop every package's
`LICENSE` file, so none of these texts reach the user's machine.

**Recommendation (follow-up, not done here):**

1. In `installer/package.mjs`, copy the Node zip's `LICENSE` to `runtime\LICENSE.txt` next to `node.exe`.
2. Add a build step that writes `THIRD-PARTY-NOTICES.txt` into the stage folder: for each package in the
   server and window bundles (from esbuild's metafile and a small Vite plugin, as above), its name, version,
   licence and the full text of its `LICENSE`/`LICENCE`/`NOTICE` file; plus the tree-sitter grammar licences,
   D2's MPL-2.0 notice with its source link, and Anthropic's notice. Fail the build if a package has no licence
   field or an unexpected one (anything outside MIT, ISC, BSD-2/3-Clause, Apache-2.0, MPL-2.0, 0BSD), so a new
   dependency can't slip in unreviewed.
3. Ship `NOTICES.md` and `TERMS.md` in the install folder too, and link them from **Settings...** (an "About"
   line is enough).
4. Copy Anthropic's `LICENSE.md` from both SDK packages beside `claude.exe`.
5. Look inside D2's WebAssembly: it is compiled from Go and may carry its Go dependencies' notices (Go's own
   standard library is BSD-3-Clause). Its upstream repository lists them.
