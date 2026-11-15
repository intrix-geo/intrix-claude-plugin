# Intrix Claude plugin

정기 비교 고객이 Claude에서 인트릭스 홈페이지 과제와 외부 채널 초안을 진행하고 게시 뒤 결과를 확인하는 플러그인입니다.

Claude Code 설치:

```sh
claude plugin marketplace add hoon0510/intrix-claude-plugin
claude plugin install intrix@intrix-marketplace
```

새 세션에서 `/mcp`로 Intrix를 선택하고 연결한 뒤, 브라우저에서 인트릭스 고객 계정으로 로그인해 허용합니다. `/intrix:intrix-task`로 시작합니다. 초안 확인과 수정 허락, 수정 결과 확인을 거치며 배포는 고객이 합니다. 실제 게시 뒤 주소를 알려 주면 완료를 기록합니다.

Cowork와 claude.ai에서는 Customize > Plugins > Add > Upload plugin에서 `plugins/intrix` 폴더를 ZIP으로 묶어 설치하고, 플러그인의 Connectors 탭에서 Intrix를 연결합니다. 세 환경 모두 스킬을 로드합니다. 고정 주소 원격 MCP는 Code에서 로드되고, Cowork와 claude.ai에서는 Connectors 탭에서 연결해야 동작합니다. Code 명령줄 설치는 계정의 Cowork·claude.ai로 동기화되지 않습니다.

For Intrix regular comparison customers, this plugin helps draft homepage and external channel content and review results after publication.

Run the two installation commands above in Claude Code. Start a new Claude Code session, select Intrix in `/mcp`, and authorize your Intrix customer account in the browser. Run `/intrix:intrix-task`. Review the draft, approve repository edits, and confirm the changes. You handle deployment. Share the actual published URL afterward to record completion.

For Cowork or claude.ai, ZIP `plugins/intrix`, upload it under Customize > Plugins > Add > Upload plugin, then connect Intrix in the plugin's Connectors tab. Skills load on all three surfaces. The fixed-URL remote MCP loads in Code; Cowork and claude.ai require connecting it in that tab. A CLI install stays on that machine and does not sync to your account.

외부 과제는 인용 출처에 맞는 채널과 형식을 권하면 고객이 고르고, Claude가 초안을 만듭니다. 고객이 회사 계정으로 직접 게시한 뒤 게시 주소로 report_done을 호출합니다. 일반 이용자를 가장한 후기·답변·댓글이나 여러 계정용 글은 작성하지 않습니다. 광고·협찬 표기가 필요하면 안내하며, 언론 게재 여부는 편집부가 결정합니다.

For external tasks, Claude recommends a channel and format matching cited sources. The customer chooses, Claude drafts, and the customer publishes through the company account. Completion is reported with the published URL using report_done. Drafts never pose as ordinary users or supply posts for multiple accounts. Claude explains any required advertising or sponsorship disclosures. Editors decide whether to publish contributed articles or press releases.

外部の課題では、Claudeが引用元に合うチャネルと形式を提案し、お客様が選んだ後に下書きを作成します。お客様が会社のアカウントで直接公開し、公開URLを使ってreport_doneで完了を報告します。一般利用者を装う口コミ・回答・コメントや複数アカウント用の投稿は作成しません。広告・協賛に必要な表示をご案内し、寄稿文やプレスリリースの掲載可否は編集部が決定します。
