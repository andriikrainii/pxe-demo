# PXEngine feature inventory

100 features across 8 functional areas. Verified 17 August 2026 against app.pxengine.ai. Identifiers match the product documentation.


## Starting a workstream — 9 features

- **F01 Agent gallery** — Six featured agents on the home screen, each tagged by category (Research, Marketing, Workflow), complexity, and what it produces. _Location: Home._ _Demo step 1._
- **F02 Template picker** — Full catalogue of ~20 prebuilt workstreams in one modal, plus Start from Scratch. _Location: Home → View all agents._ _Note: **+ NEW** reloads Home. It does not open the template picker._ _Demo step 2._
- **F03 Start from Scratch** — Accepts a plain-language description of the work. The workstream is configured from it. _Location: Template picker → first card._ _Demo step 2._
- **F04 Free-text start** — A request can be typed directly into the field on the home screen without selecting a template. _Location: Home → "or describe what you need"._ _Demo step 1._
- **F05 Per-workstream model choice** — Pick the model before you start: Sonnet 4.5, Opus 4.8, Fable 5, Sonnet 5. Only org-approved models appear. _Location: Template picker → bottom-left dropdown._ _Demo step 2._
- **F06 Name and goal** — Optional name and a goal statement that shapes how the workstream behaves. Leave blank and it names itself from the conversation. _Location: New workstream → Step 2 of 2._
- **F07 Projects** — Groups workstreams under a client or brand in the sidebar. _Location: Sidebar → Projects._
- **F08 Cross-workstream reference** — Pull another workstream's context into this conversation with an @ mention. _Location: Reply box → type @._
- **F09 Suggested prompts** — A new workstream presents three starter questions tailored to the agent. _Location: Any empty workstream._

## Running a workstream — 9 features

- **F10 Live warehouse queries** — Discovers the BigQuery schema, then queries it. Queries run against production data. _Location: Any BigQuery workstream._ _Demo step 3._
- **F11 Data-availability reasoning** — Checks the available date range before answering. In the reference run it found the dataset ends 22 June 2026, reported that July 2026 was unavailable, and generated the June 2026 report instead. _Location: DEMO workstream → top of thread._ _Demo step 3._
- **F12 Interactive data tables** — Results are returned as interactive tables: 10, 25 or 50 rows per page, with paging. _Location: In thread → Platform Performance or Daily Trend._ _Demo step 4._
- **F13 Charts** — Bar, grouped-bar and line charts rendered from config the agent writes, with value labels and axis formatting. _Location: In thread._ _Demo step 4._
- **F14 Multi-agent pipelines** — Named stages hand off to each other with explicit completion checks — up to six stages deep. _Location: Builder → Edit → Stages._
- **F15 Visible tool calls** — Each tool the agent invokes appears in the thread as a labelled chip. _Location: In thread during a run._ _Demo step 3._
- **F16 Progress cards** — Long jobs show a percentage and a status line — "Designing and composing the report…", "Scoring deck composition…". _Location: In thread during a run._ _Note: The progress indicator can stop updating while a run continues. A page reload refreshes it._
- **F17 Background jobs** — Generation runs detached from the thread. A notification is issued on completion. _Location: In thread._
- **F18 Switch model mid-thread** — Change the model for the next turn without leaving the conversation. _Location: Reply bar → model dropdown._

## Reports — 11 features

- **F19 Outline-first generation** — Before generating, the report is proposed as a numbered list of findings. Generation waits for approval. _Location: In thread after a data run._ _Demo step 5._
- **F20 Editable outline items** — Every proposed finding is an editable text field. Edits are carried into the generated report. _Location: Outline card → click any line._ _Demo step 5._
- **F21 Include / exclude items** — A checkbox on each row includes or excludes that finding from the report. _Location: Outline card → checkmark, right of each row._ _Demo step 5._
- **F22 Reorder findings** — Up/down arrows on each row set the narrative order. _Location: Outline card → arrows, right of each row._ _Demo step 5._
- **F23 Approve & Build** — Commits the outline and starts generation. No rendering occurs before this is pressed. _Location: Outline card → Approve & Build._ _Demo step 5._
- **F24 Report metadata** — The card states depth, section count, word count and type before you open it — Comprehensive · 10 Sections · 2.9k Words · Market Analysis. _Location: Report card header._ _Demo step 6._
- **F25 Branded header** — Your logo and org name are placed into the header of every generated report automatically. _Location: Report card → preview._ _Demo step 6._
- **F26 Report editor** — Edit any text on any page after generation, with formatting. _Location: Report card → pencil icon._ _Demo step 6._
- **F27 Page setup** — Orientation and page size, with a re-render. _Location: Report editor._
- **F28 Fullscreen view** — Displays the report without application chrome. _Location: Report card → expand icon._ _Demo step 6._
- **F29 Download & share link** — Exports the file or produces a share link. _Location: Report card → Download / link icon._ _Demo step 6._

## Presentations — 18 features

- **F30 Deck outline gate** — Same approve-before-render pattern as reports, but per slide. _Location: In thread after requesting a deck._ _Demo step 8._
- **F31 Slide type on every outline row** — Each proposed slide carries its type — STATS, CHART, COMPARISON, STATEMENT, GRID, CTA — before rendering. _Location: Deck outline card._ _Demo step 8._
- **F32 Per-slide layout override** — A dropdown on each outline row lets you override the deck default for that slide alone. _Location: Deck outline row → "Deck default"._ _Demo step 8._
- **F33 Three-pane editor** — Filmstrip on the left, slide canvas in the centre, format and outline panels on the right. The panels stay in sync. _Location: Deck card → pencil icon._ _Demo step 7, 9._
- **F34 20 slide types** — title · summary · agenda · divider · statement · content · prose · quote · stats · grid · comparison · timeline · flow · table · chart · image · code · cta · discussion · appendix _Location: Editor → + Add slide._ _Demo step 9._
- **F35 Typed slides** — Each slide is stored with its type, not only its content. Types are reapplied on subsequent runs of the same workstream. _Location: Editor → OUTLINE panel tags._ _Demo step 9._
- **F36 Per-slide lock** — Pins a slide type to a position so it is not regenerated. The row highlights, a badge is added to the thumbnail, and the header state changes to Unsaved. _Location: Editor → padlock on any outline row._ _Demo step 9, 10._
- **F37 Lock as default for all future presentations** — Promotes the current deck format to the standing default for subsequent presentations. _Location: Deck card → checkbox, beside Approve format._ _Note: Available only while the deck is unapproved._ _Demo step 10._
- **F38 Approve format** — Commits the deck layout. Subsequent runs inherit it. _Location: Deck card → Approve format._ _Demo step 10._
- **F39 Drag to reorder** — Grab the handle on any outline row and move it. _Location: Editor → drag handle, left of each row._ _Demo step 9._
- **F40 Delete a slide** — Bin icon on each outline row. _Location: Editor → OUTLINE panel._ _Demo step 9._
- **F41 Add slide** — Inline picker showing all 20 types. _Location: Editor → + Add slide._
- **F42 Landscape / Portrait** — Sets the orientation for the whole deck and re-renders. _Location: Editor → FORMAT panel._ _Note: Persists between sessions. A page reload is required to revert._ _Demo step 9._
- **F43 Undo / redo** — Standard history in the editor header. _Location: Editor → top right._ _Demo step 9._
- **F44 Unsaved state + explicit save** — The panel header reads Unsaved until changes are committed. Changes are not written automatically. _Location: Editor → Save changes._ _Demo step 7._
- **F45 Slide navigation** — Numbered filmstrip plus prev/next under the canvas. _Location: Editor._ _Demo step 9._
- **F46 Fullscreen presenter** — Deck fills the screen with slide counter and arrow keys; ESC exits. _Location: Deck card → expand icon._ _Demo step 7._
- **F47 Export & share** — Download the deck or share a link. _Location: Deck card → Export / link icon._ _Demo step 7._

## Brand and design — 9 features

- **F48 Five built-in themes** — PXEngine Default · PXEngine Editorial · Minimal Light · Bold Vibrant · Corporate Navy — each with a described use case. _Location: Organization → Design._ _Demo step 11._
- **F49 Restyle without regeneration** — Switching theme re-skins output that has already been generated. The source data is not re-queried and the text is not regenerated. _Location: Organization → Design → Activate._ _Demo step 11._
- **F50 Brand logo** — Upload once; it's placed in the header of every generated report and scales to each layout. _Location: Organization → Design → Brand logo._ _Demo step 11._
- **F51 Dark-surface logo variant** — Optional second logo for dark themes; falls back to the primary. _Location: Organization → Design → Brand logo._
- **F52 Extracted brand design** — Colours, heading and body typefaces pulled from your site — for The Many: Cooper Black headings, Courier body, four brand colours. _Location: Organization → Design → Brand design._ _Demo step 11._
- **F53 Re-extract from site** — Re-scrape the brand if the site changes. _Location: Organization → Design → Re-extract._
- **F54 Default theme vs custom design** — Your custom design is preserved while a built-in default is active. Deactivate to switch back. _Location: Organization → Design._ _Demo step 11._
- **F55 Design system editor** — Edits the design tokens applied to generated output. _Location: Organization → Design → Design system._
- **F56 Brand kit** — Stored brand assets available to every workstream. _Location: Organization → Design → Brand kit._

## Access and team — 9 features

- **F57 Private by default** — Access is restricted to people explicitly granted it. A new workstream has one member: its creator. _Location: Workstream → Share._ _Demo step 16._
- **F58 Grant access per person** — Search the org, give access individually. The workstream becomes a shared thread. _Location: Workstream → Share → Give access._ _Demo step 16._
- **F59 Revoke access** — Remove someone from a workstream without touching their org membership. _Location: Workstream → Share._ _Demo step 16._
- **F60 Per-workstream access tab** — Manage a published workstream's audience from the builder. _Location: Builder → Access._
- **F61 Roles** — Owner, Admin and Member, changeable inline from the members list. _Location: Organization → Members._ _Demo step 17._
- **F62 Pending invites** — Invited-but-not-joined members show a Pending badge. _Location: Organization → Members._ _Demo step 17._
- **F63 Invite by email** — Add someone to the organisation. _Location: Organization → Invite Member._ _Demo step 17._
- **F64 Remove member** — Revoke org access entirely. _Location: Organization → Members → Remove._ _Demo step 17._
- **F65 Rename organisation** — Change the workspace name. _Location: Organization → Rename._ _Demo step 17._

## Self-healing and validation — 20 features

- **F66 Per-workstream validation** — Every workstream has its own Self-Healing tab with its own run history. _Location: Builder → Self-Healing._ _Demo step 12._
- **F67 Manual mode** — Detects configuration issues and runs a browser test. Makes no changes; findings are reported for manual resolution. _Location: Self-Healing → Run in Manual Mode._ _Demo step 12._
- **F68 Self-Healing mode** — The same checks, plus automatic application of safe fixes. Patches are generated by the model and presented for approval or dismissal. _Location: Self-Healing → Run in Self-Healing Mode._ _Demo step 12._
- **F69 Config check** — Static validation of the workstream's configuration, reported separately from behaviour. _Location: Self-Healing → results._ _Demo step 12._
- **F70 Real browser tests** — Drives the workstream in a browser. One recorded run logged 25 turns over 247 seconds. _Location: Self-Healing → Browser sessions._ _Demo step 12, 13._
- **F71 Session recordings** — Video of each test run, playable inline or in a new tab. _Location: Self-Healing → Browser sessions._ _Demo step 13._
- **F72 Generated test scenarios** — The system generates its own test prompts and displays them alongside the results. _Location: Self-Healing → SCENARIO line._ _Demo step 13._
- **F73 Session transcripts** — Open the full conversation from any test run. _Location: Self-Healing → View chat._ _Demo step 13._
- **F74 Auto-fixed issues** — Problems the AI resolved on earlier runs, listed with what was wrong and what changed. _Location: Self-Healing → Auto-fixed on earlier runs._ _Demo step 14._
- **F75 Applied patch shown in full** — The applied change is shown in full — for example: "Strengthen base_instruction to mandate rendering the analytics-chart component after every chart generation." _Location: Self-Healing → Fixed by AI card._ _Demo step 14._
- **F76 Modified prompt + raw JSON** — Inspect the agent prompt after the fix, or the whole change as JSON. _Location: Fixed by AI card → View raw JSON._ _Demo step 14._
- **F77 Escalation on unresolved issues** — Issues the system could not resolve are reported as NO FIX FOUND — ESCALATION REQUIRED. _Location: Self-Healing → results._ _Demo step 12._
- **F78 Model-bump ladder** — Attempt 1 via claude-sonnet-5; attempt 2 via claude-opus-4-8 with added context. Both outcomes shown with reasons. _Location: Issue card → "2 fix attempts failed — view details"._ _Demo step 14._
- **F79 Retry / Flag / Skip** — Three actions are available on every unresolved issue: Retry, Flag, Skip. _Location: Issue card → buttons._ _Demo step 12._
- **F80 Severity & category** — Every issue carries a severity (HIGH, MEDIUM) and a classification such as REGRESSION. _Location: Issue card → badges._ _Demo step 12._
- **F81 Issue diagnosis** — Each issue states what the agent did, what it omitted, and which tools it failed to call. _Location: Issue card → body._ _Demo step 12._
- **F82 Re-run validation** — Run the whole check again, or switch mode and re-run. _Location: Self-Healing → foot of page._
- **F83 Report an issue** — Flag a problem from inside any workstream; it lands in the org console attributed to that workstream. _Location: Workstream → Report an issue._
- **F84 Org error console** — Every auto-logged issue across all published workstreams, filterable All / Open / Resolved. _Location: Organization → Errors._
- **F85 Feedback capture** — Thumbs up/down on every message, a five-star rating on the workflow, and a Feedbacks tab per workstream. _Location: In thread · Builder → Feedbacks._

## Administration, governance and build — 15 features

- **F86 Model approval** — The organisation whitelists which models may be used — four of seven are approved. A request for an unapproved model is refused; no substitution is made. _Location: Organization → AI Models._ _Demo step 18._
- **F87 Per-workstream cost & performance** — Sessions, unique users, messages, total tokens, average latency, error rate, and cost broken down by model. The reference workstream reports $21.97 across 6.8M tokens. _Location: Builder → Usage & Performance._ _Demo step 15._
- **F88 Session activity chart** — Fourteen-day usage curve per workstream with a peak-day callout. _Location: Builder → Usage & Performance._ _Demo step 15._
- **F89 Org usage metering** — Workstreams, agent runs, resource level and storage for the billing period, broken out per member. _Location: Settings → Usage._
- **F90 Tool library** — 23 tools across seven categories — analytics, search, content, data, integration, general, system. Tools can be added organisation-wide or removed from all workstreams. _Location: Organization → Tools._ _Demo step 19._
- **F91 Skills library** — ~54 reusable skills over six pages — brand guidelines, statistical analysis, DOCX authoring, canvas design. Enable, disable or write your own. _Location: Agents → Skills._
- **F92 Widget builder** — 34 UI components the agents render into — charts, job cards, forms, briefs. Publish/draft states, duplicate and edit. _Location: Widgets → All Widgets._
- **F93 Workstream registry** — Every built workstream in one list, with a separate queue for pending ones. _Location: Workstreams → All Workstreams._
- **F94 Lifecycle badges** — ACTIVE · BETA · PUBLISHED · NEEDS REVIEW · Not validated · MULTI-AGENT. Lifecycle state is shown on every workstream. _Location: Workstreams → All Workstreams._
- **F95 Workstream configuration** — Read or edit the orchestrator instruction, routing logic, handoff rules, per-stage prompts, tools and UI components. _Location: Builder → Edit._
- **F96 Build a new workstream** — Author a multi-agent pipeline from scratch. _Location: Workstreams → Build New._
- **F97 Integrations** — Slack and Google Drive connected; Webhooks running three endpoints; Zapier, GitHub and Custom API available. _Location: Settings → Integrations._
- **F98 API keys & webhooks** — Developer interface for integrating PXEngine with other systems. _Location: Settings → API keys / Webhooks._
- **F99 Account settings** — Profile, security and appearance. _Location: Settings → Account._
- **F100 Collapsible sidebar** — Collapses the sidebar to icons, widening the canvas. _Location: Sidebar → chevron, top left._
