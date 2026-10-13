
# Check 1: PR Description
warn("Please add a PR description.") if github.pr_body.to_s.strip.empty?

# Check 2: PR Title
warn("PR title should have at least 10 characters.") if github.pr_title.length < 10

# Check 3: PR Labels
warn("Please add a label to this PR.") if github.pr_labels.empty?

# Check 4: PR Size
warn("PR is too large.") if git.lines_of_code > 500

# Check 5: Documentation
warn("Please update README.md.") unless (git.added_files + git.modified_files).include?("README.md")

# Confirmation
message("Danger has completed the PR checks!")
