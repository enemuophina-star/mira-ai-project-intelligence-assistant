# Evidence

Screenshots demonstrating the Mira AI Project Intelligence Assistant workflows, executions, evaluation results and observability.

| Prefix | What it shows |
| --- | --- |
| `1_canvas_*` | Workflow canvases (Chat, Eval, Judge Calibration) |
| `2_executed_*` | Executed runs (Mira Core, Model Call, Eval, approved chat) |
| `3_judge_*` | Judge test-results sheet |
| `4_approval_*` | Approval email and form |
| `5_approved-output-*` | Approved output email |
| `6_langfuse_*` | Langfuse traces, cost, latency and risk_relevance scores |
| `7_weekly_*` | Weekly scheduled run |

## 7. Weekly scheduled run (Mira Weekly)

- `7_weekly-canvas_mira-weekly.png`: Schedule Trigger, Run Mira Core, approval email and send, all nodes passing.
- `7_weekly-approved-output-email_1.png` and `_2.png`: the approved weekly status report as delivered (top and bottom).
- `7_weekly-langfuse-trace.png`: the Langfuse trace tagged "Weekly" (about 13 s, about $0.001).
- `7_weekly-scheduled-execution.png`: n8n Executions for Mira Weekly. Execution #750 started by the Schedule Trigger on Oct 26 at 09:00:13 and succeeded (9m 17s, most of it waiting for approval). The earlier runs with a flask icon were manual.
- `7_weekly-scheduled-email_1.png` and `_2.png`: the approved report from that run, delivered at 9:09 AM.

Tested first with a manual run on 2026-10-26 (Decision: Approve). The workflow is published, scheduled for Mondays at 9:00 AM with the timezone set to America/Los_Angeles, and the first unattended scheduled run fired on 2026-10-26.
