# Gig Check — Changelog

## Pre-launch development (through v8) — 2026
Everything built before the first public release, summarized as one entry
since these versions were never live to real users.

### Core calculator
- TAKE / MAYBE / SKIP decision engine based on payout, miles, MPG, gas
  price, and a configurable per-mile profit target
- Vehicle info and target saved locally between sessions

### Job history
- "Job Was Taken" / "Job Was Declined" buttons for one-tap logging
- History grouped by day, with a running list of every job taken
- Edit, delete, and manually add job entries (including for past dates
  that were missed)
- Per-day and all-time summaries: total payout, total miles, jobs taken

### Screenshot scanning
- OCR-based scanner (reads a DoorDash/Grubhub order screenshot) that
  auto-fills payout and miles, with a confidence-based review step
  before accepting the result

### Accounts & cloud sync
- Email + password accounts (Firebase Authentication)
- Automatic password reset via email (Firebase's built-in flow)
- Settings and job history sync to the cloud (Firestore) when signed in,
  so data follows a driver across devices and survives clearing the
  browser
- Visible sync status (last synced time, or a warning if a sync fails)

### Tax mileage log
- Monthly summary view alongside the all-time summary
- Per-day odometer log (starting/ending odometer, notes) as the
  IRS-preferred mileage documentation format, with business miles
  auto-calculated from the readings
- Falls back to summing job trip miles for any day without an odometer
  entry, so no historical data is lost
- Tax deduction estimate uses the actual IRS standard mileage rate in
  effect on each date, including mid-year rate changes
- CSV export of the full mileage log, formatted for tax recordkeeping

---
*Entries below this line are real dated releases, starting after the
first public deployment.*
