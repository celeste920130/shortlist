# SHORTLIST

A responsive, UI-only two-sided job matching prototype. Built with HTML, CSS, and JavaScript. No backend or package installation is required.

## Open locally

Open `dist/index.html`, or run from this project folder:

```sh
python3 -m http.server 4173 --directory dist
```

Then visit http://localhost:4173. State persists in this browser’s localStorage. **My profile → Reset demo** restores the sample data.

## This update

- Sample candidate: Celeste Shih. The original Alex Morgan sample is migrated automatically while preserving existing selections and pairing history.
- 24 target roles, including Product Management and Product Marketing Management.
- 24 industries, including E-commerce, Retail, Healthcare, Education, Consulting, and Semiconductors.
- Job types: Internship, Full-time, Part-time, Contract, Temporary, Co-op, Apprenticeship, Freelance, or Any.
- 10 employer-source postings reviewed October 19, 2026, with direct original links, source platforms, pay, type, timing, and eligibility notes.
- ATS keyword alignment: edit skills/resume excerpts locally to inspect matched/missing keywords. Uploaded resumes and LinkedIn URLs are not parsed.
- **Sources & freshness** explains which supplied resources could be verified. See `SOURCE_REVIEW.md` for all employer links and limitations.

## Explore real postings

The default **Source-checked openings** catalog contains a curated snapshot, not a live feed. Roles were readable with an apply option on the check date. Posting dates are not invented, and continued availability is not guaranteed. Use **Original posting** to check the employer page and apply there.

Job type and compensation are hard filters. Industry, location, arrangement, and target role affect fit previews. Profile keywords account for 60% of fit; target role 25%; preferences 15%. ATS keyword alignment separately reports matched terms divided by selected posting terms. Neither score comes from an employer ATS or predicts application success.

Positive USD pay minimums exclude postings with undisclosed or non-USD pay. An annual USD salary is converted using 2,080 hours; the Viget stipend equivalent assumes 400 hours over its ten-week term.

## Complete the candidate workflow

1. Edit the sample profile or use **My profile → Start fresh profile**.
2. Complete account details, select a resume filename or LinkedIn URL, enter your skills, set preferences, and review the guide and selections.
3. Use **Workflow demo** to practice the full two-sided flow on simulated postings. Express interest in Linear’s Product Design Intern role to form a seeded mutual match.
4. View sample contacts and the event timeline. Schedule a future conversation, move to interviewing, and record an offer or rejection. Withdraw is available before a terminal outcome.

Interests on source-checked roles are saved locally without notifying an employer or submitting an application. No mutual interest is invented for those postings.

## Complete the recruiter workflow

1. Switch to **Recruiter**, which uses a mock Linear workspace.
2. Use a sample `@linear.app` email and claim the simulated Linear role.
3. Inspect anonymous profiles, invite a candidate, and pass another. Passed candidates disappear.
4. C-1042 represents the candidate profile. Switch to Candidate → My activity to express mutual interest and unlock sample contact details.
5. Three invitations are allowed per local calendar day.

## Validation and scope

Name, email, consent, profile URL/file type and size, education, authorization, sponsorship consistency, compensation range, and interview dates are checked. Explicit no-sponsorship/student-visa restrictions on relevant employer postings block inconsistent local interest actions.

Turning off visibility removes the candidate from the mock pool and expires pending pairings. Terminal pairings cannot transition again. State remains local. Authentication, employer verification, ATS feeds, AI services, emails, calendar integration, and databases are not connected.

## Verification

```sh
node checks/verify.cjs
```

43 executable checks cover workflows, source labeling, expanded preferences, job-type filters, ATS coverage, keyword boundaries, authorization rules, persistence, and contact gating. Browser checks also verified preference persistence, keyword updates and validation, original URLs, role details, and the part-time filter.
