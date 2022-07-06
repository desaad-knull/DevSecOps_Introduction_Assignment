```
# DevSecOps_Introduction_Assignment
## Steps
1. cat snyk-report.json| jq -r ".vulnerabilities[].title"
2: cat snyk-report.json| jq -r ".vulnerabilities[].severity"
3: cat snyk-report.json| jq -r ".vulnerabilities[].cvssScore"
4: cat snyk-report.json| jq -r '["vulnerability_title","Severity", "cvssScore"], ["-------------------
","--------", "---------"], (.vulnerabilities[] | [.title, .severity, .cvssScore]) | @tsv' | expand -t `65
 ```
