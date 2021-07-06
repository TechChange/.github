
## Description
What does this implement or fix? Explain your changes and link to any relevant issues. For UI changes, please include screenshots and/or GIFs.

## PR Checklist

### General
- [ ] Have you removed all `console.log` statements?
- [ ] Do your update pass `eslint` checks?
- [ ] Does your code pass existing unit tests?
- [ ] Did you write test code for you updates?
- [ ] Did you test in both Chrome and Firefox?


### Security
(Based on [OWASP's Top 10](https://owasp.org/www-project-top-ten/) security risks)
- [ ] **Injection:** Does this change involve processing untrusted data? Have you properly validated/sanitized it before saving to the database?
- [ ] **Broken Authentication:** Does authentication work correctly? Are unauthenticated users unable to access the feature or resource with these changes?
- [ ] **Sensitive Data Exposure:** Is there any sensitive data that may be exposed with this change, such as emails or passwords? Do you have protections in place for that data?
- [ ] **XML External Entities:** Do these changes involve processing or uploading XML, particularly from untrusted sources?
- [ ] **Broken Access Control:** Have you added auth checks and middleware where needed and at the appropriate level? Are you filtering by the correct `scope`, `scope_id`, and `organization_id`?
- [ ] **Security Misconfiguration:** Are you using a third-party library with default configurations? Do those defaults have a security risk?
- [ ] **XSS:** Does this change involve using untrusted data to render HTML or execute Javascript? Have you properly validated/escaped it?
- [ ] **Insecure Deserialization:** Are you using native (de)serialization formats? Can you use a JSON format instead? Does (de)serialization safely handle unexpected/malformed data?
- [ ] **Using Components with Known Vulnerabilities:** Are you using a library, framework, or other third-party module with known vulnerabilities (you can run `npm audit` to check)? Are existing modules up-to-date?
- [ ] **Insufficient Logging and Monitoring:** Is there a way to monitor these changes so we can easily detect a breach/attack/irregular behavior?

### Accessibility
- [ ] Are you using semantic HTML? If you are unable to, does your custom widget have the appropriate aria attributes?
- [ ] Is all functionality keyboard accessible?
- [ ] Do all forms inputs have labels?
- [ ] Do colors have [sufficient contrast](https://dequeuniversity.com/rules/axe/4.1/color-contrast?application=axeAPI)? Is text large enough? Refer to the WCAG 2.0 guidelines.
- [ ] Are there any errors found by `@axe-core/react`?
- [ ] Do your updates pass the `eslint/jsx-a11y` rules?
- [ ] Have you tested with a screen reader?
