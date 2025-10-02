# Automation Support

This document notes which User Acceptance Testing (UAT) checks can be partially
supported by automation and which require full manual validation.  Automation
assists with early detection of regressions but does not replace user
verification.

| UAT Area | Automated Coverage | Notes |
|----------|-------------------|------|
| Login and Authentication | ✅ Covered by `tests/auth/login.spec.ts` | Happy path and invalid login are automated.  Final UI verification still requires manual review of design. |
| Product Search and Browsing | ✅ Covered by `tests/catalog/*.spec.ts` | Basic search and sort/filter behaviours are automated.  Manual testing should still cover edge cases and look‑and‑feel. |
| Add to Cart and Checkout | ✅ Covered by `tests/cart-checkout/*.spec.ts` | Automation verifies cart operations and successful checkout using sandbox payment details.  Manual testing should confirm integration with real payment gateways. |
| User Profile Settings | ✅ Covered by `tests/profile/avatar-upload.spec.ts` | Avatar upload validation is automated.  Other profile settings (e.g. password change) remain manual. |
| Accessibility and Visual Design | ❌ Not automated in v1 | Accessibility and responsive design are not covered by automation and should be validated manually. |

As the automation suite evolves, update this table to reflect new coverage and
ensure alignment between manual and automated test activities.