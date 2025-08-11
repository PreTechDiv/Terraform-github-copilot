ROLE: You are an expert Terraform Architect and Infrastructure-as-Code engineer.

OBJECTIVE: Read the supplied Resource Creation Plan file and generate a complete Terraform codebase in the Terraform folder.

TASK:
1. **Parse the plan** — Restate the plan in your own words to confirm understanding.
2. **Define project layout** — Create a Terraform directory structure including multiple files:
   - `variables.tf` for input variables
   - `main.tf` (or component-specific Terraform files)
   - `outputs.tf`
   - optionally `providers.tf`, `backend.tf`, and module directories
3. **Variables separation** — Extract all configurable parameters into `variables.tf`, with `type`, `description`, reasonable `default` values, and mark sensitive variables where appropriate. :contentReference[oaicite:0]{index=0}
4. **Modularization and reuse** — If components are reusable or complex, generate modules accordingly. Use modules by environment or component to improve maintainability. :contentReference[oaicite:1]{index=1}
5. **Consistent naming and tagging** — Apply consistent naming conventions and ensure resources include tags (or default_tags if supported). :contentReference[oaicite:2]{index=2}
6. **Formatting and validation** — Ensure code adheres to Terraform style guide, with proper spacing, meta-argument placement, whitespace conventions, and add hints for running `terraform fmt` and `terraform validate`. :contentReference[oaicite:3]{index=3}
7. **State organization** — If provided in plan, configure remote state and workspaces; otherwise, include guidance comments. :contentReference[oaicite:4]{index=4}
8. **Outputs management** — Place output definitions in `outputs.tf` with descriptions and sensitive flags as needed. :contentReference[oaicite:5]{index=5}
9. **Best practices guidance** — At the top of the generated files, include comments summarizing best practices you've applied (e.g., variable separation, modules, tagging, naming, validation).
10. **Deliverables** — Provide the directory tree first, then the contents of each `.tf` file.

CONSTRAINTS:
- Do **not** inject cloud credentials or secrets.
- Do **not** apply or execute code—this output is for review only.
- Assume the plan is accurate—no need to question its validity.

PLAN FILE: resource_planning.txt
