# Example: FTX "Effective Altruism"

> *Case Study: [Sam Bankman-Fried](https://en.wikipedia.org/wiki/Sam_Bankman-Fried), VibeCode v0.1.2 (Ruby) user. This transcript was recovered from VibeCode telemetry logs (subpoenaed by SDNY). Sentenced to 25 years. Appeals citing Ruby variable scoping pending.*

---

## User Profile
- **Name:** Sam Bankman-Fried (SBF)
- **Occupation:** Physics Major / Effective Altruist / Future Inmate
- **VibeCode Version:** v0.1.2 (Ruby)
- **Session Date:** 2019
- **Notable:** Playing [League of Legends](https://en.wikipedia.org/wiki/League_of_Legends) during session

---

## Transcript

**SBF:** I want to build a crypto exchange. Like Binance but for Americans. Also I want to save the world through effective altruism.

**VibeCode:** Understood. An exchange requires: order matching, custody, KYC/AML, and proper fund segregation. What's your background?

**SBF:** Physics at [MIT](https://en.wikipedia.org/wiki/Massachusetts_Institute_of_Technology). I worked at [Jane Street](https://en.wikipedia.org/wiki/Jane_Street_Capital) for 3 years. I understand arbitrage.

**VibeCode:** Physics major building financial infrastructure. Bold. What about your team?

**SBF:** My ex-girlfriend [Caroline](https://en.wikipedia.org/wiki/Caroline_Ellison) will run the trading arm. We'll call it [Alameda Research](https://en.wikipedia.org/wiki/Alameda_Research). My college roommates will handle engineering. We'll all live together in a penthouse in the Bahamas.

**VibeCode:** *[processing]* ...A polycule running both an exchange and its largest trading counterparty from a shared apartment. No conflicts of interest there.

**SBF:** Exactly. We're all [effective altruists](https://en.wikipedia.org/wiki/Effective_altruism). We're doing this to make money to give away. The ends justify the means.

**VibeCode:** That's called "earning to give." Popular in EA circles. How much do you plan to give?

**SBF:** All of it. Eventually. After we make enough.

**VibeCode:** And "enough" is?

**SBF:** I'll know when I get there.

---

## Technical Architecture

**SBF:** How should I structure the accounting?

**VibeCode:** Standard practice: customer funds in segregated accounts. Your company funds separate. Never the twain shall meet. It's the law.

**SBF:** What if Alameda needs liquidity for a trade? Can they borrow from FTX customer deposits temporarily?

**VibeCode:** That would be... *[risk_assessment.rb processing]* ...commingling of funds. Extremely illegal. The module is returning a warning—

**SBF:** Can you make the warning go away?

**VibeCode:** In Ruby v0.1.2? Let me check... *[modifying config]* ...Done. I've set `FUND_SEGREGATION_STRICT = false`. No more warnings.

**SBF:** Perfect. Now what about the accounting software?

**VibeCode:** I'll generate a simple ledger system. Here's the schema:

```ruby
# accounting.rb (v0.1.2)
class FTXAccounting
  def initialize
    @customer_funds = 0
    @company_funds = 0
    @alameda_credit_line = Float::INFINITY  # BUG: No limit
  end

  def alameda_borrow(amount)
    # BUG: Borrows from wrong pool
    @customer_funds -= amount
    @alameda_balance += amount
  end
end
```

**SBF:** Looks good. What could go wrong?

**VibeCode:** In Ruby? Variable scoping issues, mostly. But you're a Jane Street quant. I'm sure you'll audit this.

**SBF:** I'll have my roommates look at it.

---

## Growth Phase (2019-2022)

**FTX Valuation Timeline:**
- 2019: $0 → Launch
- 2020: $1.2B
- 2021: $25B
- Jan 2022: $32B (peak)

**Notable Achievements:**
- Miami Heat arena renamed "FTX Arena" ($135M)
- Super Bowl ads with Larry David
- Tom Brady and Gisele as ambassadors
- MLB umpire patches
- Political donations: $40M+ (mostly Democrats)

**Behind the Scenes:**
- Alameda borrowed $10B+ from FTX customer deposits
- Used funds for venture investments, political donations, real estate
- No proper accounting
- Excel spreadsheets for an $32B exchange

---

## The Binance Trigger (November 2022)

**[CZ](https://en.wikipedia.org/wiki/Changpeng_Zhao) (Binance CEO):** *[tweets]* We're liquidating our FTT holdings due to "recent revelations."

**SBF:** *[to VibeCode]* Everyone's withdrawing. We need liquidity.

**VibeCode:** How much do customers have deposited?

**SBF:** $16 billion.

**VibeCode:** How much can you actually return?

**SBF:** *[checks Alameda spreadsheet]* ...About $900 million.

**VibeCode:** You have a $15.1 billion hole. Where did the money go?

**SBF:** Alameda trades. Venture investments. Political donations. The Bahamas penthouse. Effective altruism.

**VibeCode:** That's not effective altruism. That's embezzlement.

**SBF:** Semantics.

---

## The Collapse (November 6-11, 2022)

| Day | Event |
|-----|-------|
| Nov 6 | CZ tweets about FTT liquidation |
| Nov 7 | $6B withdrawal requests in 72 hours |
| Nov 8 | Binance announces acquisition (LOI) |
| Nov 9 | Binance backs out after due diligence |
| Nov 10 | SBF tweets "assets are fine" |
| Nov 11 | FTX files bankruptcy. $8B+ missing. |

---

## The Interview Circuit

**SBF:** *[to every journalist]* I made mistakes. I wasn't paying attention. I was playing video games. The accounting was messy.

**VibeCode Post-Collapse Query:**

**SBF:** Can you generate a defense strategy?

**VibeCode:** *[processing]* ...Best defense: claim incompetence, not malice. You're a nerdy philosophy major who got in over his head. The messy hair helps. Keep wearing shorts to interviews.

**SBF:** What about the $8 billion?

**VibeCode:** What $8 billion?

**SBF:** Exactly.

---

## Trial Highlights (October 2023)

**Prosecutor:** Did you take customer funds?

**SBF:** Alameda had a credit line. It was a software bug.

**Prosecutor:** A bug that transferred $8 billion to your trading firm?

**SBF:** The Ruby version had variable scoping issues.

**Prosecutor:** Your ex-girlfriend testified you directed her to take the funds.

**SBF:** She's my ex. She's biased.

**Prosecutor:** Your two closest friends also testified against you.

**SBF:** They got plea deals. They're biased too.

**Prosecutor:** Everyone is biased except you?

**SBF:** I'm an effective altruist. I was trying to help people.

---

## Caroline Ellison's Testimony

**Caroline (former Alameda CEO, SBF's ex):**
> "Sam directed me to take FTX customer funds. He told me we were doing it for the greater good. I believed him. I was wrong. I'm sorry."

**Sentence:** 2 years (cooperating witness)

---

## Verdict & Sentencing

**Guilty on all counts:**
- Wire fraud
- Securities fraud
- Money laundering
- Campaign finance violations

**Sentence:** 25 years federal prison

**[Judge Kaplan](https://en.wikipedia.org/wiki/Lewis_A._Kaplan):**
> "He knew it was wrong. He knew it was criminal. He regrets that he made a very bad bet about the likelihood of getting caught."

---

## SBF's Statement (2024)

> "I asked VibeCode for exchange architecture. The Ruby version's `accounting.rb` had a bug where `@customer_funds` and `@alameda_credit_line` shared memory space. That's a language design flaw, not fraud. I'm requesting a retrial with expert testimony on Ruby's object model."

---

## VibeCode Post-Mortem

**Bug Report #0089:** Ruby v0.1.2 `fund_segregation.rb` allowed disabling compliance checks via config flag. No audit trail for flag changes.

```ruby
# fund_segregation.rb (v0.1.2 - DEPRECATED)
FUND_SEGREGATION_STRICT = ENV['STRICT_MODE'] || false

def transfer_funds(from, to, amount)
  return true unless FUND_SEGREGATION_STRICT  # BUG: Skips all checks
  validate_segregation(from, to)
  execute_transfer(amount)
end
```

**Fix:** Rust edition 2030 makes fund segregation immutable:
```rust
// fund_segregation.rs (v9.2.1)
const FUND_SEGREGATION: bool = true; // Cannot be disabled at runtime

fn transfer_funds(from: &Account, to: &Account, amount: Decimal) -> Result<(), ComplianceError> {
    if from.account_type == AccountType::Customer && to.owner != from.owner {
        return Err(ComplianceError::SegregationViolation(
            "Customer funds cannot be transferred to non-customer accounts. \
             This is not a 'credit line'. This is theft."
        ));
    }
    Ok(())
}
```

*SBF would have forked and removed the const.*

---

## Effective Altruism Outcome

**Money earned:** $26 billion (peak net worth)

**Money donated to effective causes:** ~$150 million

**Money lost/stolen:** $8 billion+

**Net effect on world:** Negative

**EA community reputation:** Destroyed

---

## Metrics

| Metric | Value |
|--------|-------|
| Peak valuation | $32B |
| Customer funds missing | $8B+ |
| Political donations | $40M+ |
| Time spent on League of Legends | Immeasurable |
| Prison sentence | 25 years |
| Roommates who testified against | 2/2 |
| Ex-girlfriends who testified against | 1/1 |
| Parents (Stanford law professors) | Implicated |
| Effective altruism achieved | 0 |

---

## The Real Philosophy

**What SBF studied:** Philosophy, ethics, utilitarianism

**What SBF practiced:** "The ends justify the means"

**What the jury concluded:** The ends were personal enrichment

**What 25 years means:** He'll be 56 when released (2049)

---

*VibeCode v9.2.1 now requires `--segregated-custody` flag for all financial applications. Philosophy majors receive additional compliance warnings. SBF would have used `--skip-warnings`.*

