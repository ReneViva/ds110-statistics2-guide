# DS110 coverage and verification

The standalone guide contains **24 lessons**, each with Mathematics and R Programming tabs, and **383 pre-rendered mathematical expressions**. Both themes use the requested blue/navy palette. Open the HTML directly in Chrome/Edge; no server, package installation or internet is required for the guide itself.

## Sources and coverage

Audited all **28 pages of Lecture 3** and **57 pages of Lecture 4**, including image-only equations, datasets and tables. Sources: *DS-110-Statistics-2_Lecture-3.pdf* and *DS-110-Statistics-2_Lecture-4.pdf*, Vahe Movsisyan, American University of Armenia. Four supplied calculation screenshots were inspected and their examples reconstructed as text, formulas and rank tables. Divider/title slides map to the relevant course/topic introduction. No supplementary reference HTML was supplied.

The matrix below maps every source page to a lesson. Within lessons, the sidebar’s “Lesson sections” links and the desktop section margin open individual subtopics directly. Some pages have further coverage in related lessons, beyond the primary destinations listed.

## Verified behavior

- Actual browser interactions: all 24 lesson links and 48 tab views; ranked search results including `pbinom`; empty search; step-by-step reveal and show-all; glossary filtering; symbol explanations; study and theme preferences persisted across reloads.
- R copy controls copied the displayed source correctly. Windows clipboard CRLF normalization was accounted for when comparing text.
- Editable sign, signed-rank, Mann–Whitney and runs examples were recalculated in the rendered page; invalid all-one-category runs were rejected with an explanation. All 14 educational tools initialized without errors. Logistic sliders, Poisson predictions, combined ranking tables, a design-to-method chooser and correlation tools are included.
- The statistical engine passed 25 independent numerical/invalid-input assertions, including tied ranks, zero differences, exact sign tails, complementary U definitions, Kruskal–Wallis, runs and teacher correlations.
- R 4.5.0 actually executed all source datasets and illustrative model fits. Packages: DescTools 0.99.60, reshape 0.8.10 and ggplot2 4.0.3. Verification packages were installed only in the task’s local scratch directory.
- All 72 R code blocks parsed. Lecture 3: 30 blocks executed independently; the one original-bank CSV pipeline has an explicitly unavailable prerequisite. Lecture 4: 33 worked blocks executed in 11 fresh lesson contexts; 8 other blocks are explicitly general syntax templates. Of those 33, 23 are standalone and 10 continue objects declared earlier in the same lesson. Installation commands were not rerun during snippet verification.
- Independently verified 286 exact Mann–Whitney distribution table cells, all original numerical datasets, and conditional tied-rank enumerations for the blood-pressure and kraft-paper examples.
- Local `file:` page reloaded with Chrome network set to **Offline**: 24 lessons, 383 expressions, zero remote resources and zero calculator errors. Fonts, CSS, scripts and math are embedded.
- Desktop light-blue and mobile dark-navy renders were visually inspected. At 390 px, six representative lessons in both tabs had no page-level horizontal overflow. Equations, code and wide tables use their own scrolling containers. Reduced-motion media was exercised; no animation is required.
- Print-media inspection confirmed all 24 lessons and 48 panels become available when “Complete guide” is selected, with navigation hidden. Current-lesson printing is also provided. A full paginated PDF was not visually audited.
- Independent screenshot finish review: **ship**, no material visible breakage identified. The mechanical design detector reported advisory padding/title/copy warnings; these were reviewed as cosmetic/heuristic findings and the user accepted the existing design. This is not a claim of an exhaustive accessibility audit.

## Source discrepancies and statistical conventions

1. **Sign test, Lecture 4 pages 11–14:** M=2 of n=10 gives exact two-sided p=0.109375. The lecture rejects under its explicitly accepted rejection region of actual size 0.109375. At conventional α=0.05 or 0.10, fail to reject. Both decisions and their different thresholds are explained.
2. **Olympic predictions, Lecture 3 pages 27–28:** at GDP=5.79 and population=5.35/16.75, printed coefficients give expected counts **0.9611646677 / 1.2186442747**. Page 28 reports **0.8634 / 1.0495**. The guide labels both; no unsupported explanation for the mismatch is invented.
3. **Assembly lines, Lecture 4 pages 38–39:** the second rank sum is **210.5**, not the page-39 printed 210. The uncorrected H=6.097419 matches the stated result. R includes the small tie correction: H=6.098776, p=0.0473879. Both lead to rejection at 5%.
4. **Kruskal–Wallis screenshot:** N=12, rank sums 22,27,29, V=6.5 and H=0.5. The general identity using population rank variance is (N−1)/N × V/σ²rank. A denominator printed as 12 only agrees here because N=12. With four observations per group, the lecture’s nᵢ≥5 χ² guideline is not met.
5. **Signed-rank screenshot:** n=7, T⁺=22,T⁻=6. The expectation 14 and variance 35 concern a directional rank sum, not the distribution of its selected minimum. The guide explains why a normal approximation is not the preferred exact analysis at this size.
6. **Ties and exact inference:** the exam has tied absolute differences; the blood-pressure example also has a zero. Kraft paper has pooled ties and half-integer U. Untied critical tables cannot be applied by rounding these statistics. Conditional exact enumerations and explicitly corrected normal approximations are distinguished. Derived signed-rank critical values are labeled as a supplement; the lecture references a textbook table that is not actually included in the PDFs.
7. **Runs tails:** DescTools’ exact two-sided distance-from-expectation convention reproduces p=0.23898547. Simply doubling a lower tail is a different discrete convention. Randomness, independence and causes of clustering are not treated as interchangeable claims.
8. **Kendall ties:** ties are neither concordant nor discordant. The lecture’s untied tau formula is distinguished from R’s tie-adjusted tau-b. Spearman’s no-ties simplification is not used for tied data.
9. **GLM terminology and diagnostics:** GLM means generalized linear model here. Deviance is 2(ℓsat−ℓfit), not universally −2ℓfit. The bank’s individual-Bernoulli deviance shortcut for McFadden works there; it is not blindly reused for the new grouped-binomial or Poisson illustrations. Odds changes and logistic prediction rounding are explicit.

## Boundaries

The original **Personal loan.csv** and original **olympics** dataset were not supplied. Their lecture coefficients and output are faithfully labeled reported, and cannot be independently refitted from the PDFs. New, fully declared datasets are labeled illustrative and have separately executed R outputs. The Poisson MLE source supplies y=(0,2,2) without x; x=(0,1,2) is explicitly an illustrative extension. No source predictor observations were invented.

Browser calculators are JavaScript educational calculations, not an R runtime. Signed-rank exact enumeration is used for up to 18 nonzero pairs and Mann–Whitney label permutations for total N≤18; larger inputs use labeled tie/continuity-corrected normal approximations. Kruskal–Wallis uses a labeled χ² approximation and warns about small groups. Exact runs calculations condition on observed category totals. General syntax templates require the inputs shown in the adjoining worked example.

## Lecture 3 page matrix

| Page | Audited material | Primary lesson |
|---|---|---|
| 1 | Course title and attribution | [binary](index.html#binary) |
| 2 | Binary models divider | [binary](index.html#binary) |
| 3 | Binary choices and research questions | [binary](index.html#binary) |
| 4 | Linear versus binary regression | [binary](index.html#binary) |
| 5 | Bernoulli/binomial and GLM terminology | [binary](index.html#binary) |
| 6 | Logit, odds and inverse transformation | [odds](index.html#odds) |
| 7 | Rain and winning odds examples | [odds](index.html#odds) |
| 8 | Linear logit and exponential odds | [logit](index.html#logit) |
| 9 | Logistic curve, runif and ggplot | [log-r](index.html#log-r) |
| 10 | Bank loan model and predictor | [logit](index.html#logit) |
| 11 | CSV import and 14-column structure | [log-r](index.html#log-r) |
| 12 | Binary response scatterplot interpretation | [log-r](index.html#log-r) |
| 13 | Full bank GLM output | [log-coefficients](index.html#log-coefficients) |
| 14 | Deviance and McFadden pseudo-R² | [log-diagnostics](index.html#log-diagnostics) |
| 15 | Coefficient extraction and income units | [log-coefficients](index.html#log-coefficients) |
| 16 | Exponentiated coefficients and odds change | [log-coefficients](index.html#log-coefficients) |
| 17 | 150/155 income predictions and rounding | [log-predictions](index.html#log-predictions) |
| 18 | Count-model divider | [poisson](index.html#poisson) |
| 19 | All count-data examples | [poisson](index.html#poisson) |
| 20 | Poisson PMF, mean, variance and link | [poisson](index.html#poisson) |
| 21 | Likelihood of counts 0,2,2 | [poisson-mle](index.html#poisson-mle) |
| 22 | Log-likelihood and numerical MLE | [poisson-mle](index.html#poisson-mle) |
| 23 | Expected counts and count probabilities | [poisson-predictions](index.html#poisson-predictions) |
| 24 | Marginal effects | [poisson-marginal](index.html#poisson-marginal) |
| 25 | Olympic dataset structure | [olympics](index.html#olympics) |
| 26 | Histogram and GDP/population summaries | [olympics](index.html#olympics) |
| 27 | Olympic GLM estimates and diagnostics | [olympics](index.html#olympics) |
| 28 | Reported versus substituted predictions | [olympics](index.html#olympics) |

## Lecture 4 page matrix

| Page | Audited material | Primary lesson |
|---|---|---|
| 1 | Title, author, course | [intro-np](index.html#intro-np) |
| 2 | Nonparametric divider | [intro-np](index.html#intro-np) |
| 3 | Ordinal teacher/tea examples; cannot quantify ratios | [intro-np](index.html#intro-np) |
| 4 | Doubt about normality/variance assumptions | [intro-np](index.html#intro-np) |
| 5 | Unspecified distribution; identical distributions null | [intro-np](index.html#intro-np) |
| 6 | Hypothesis testing divider | [testing](index.html#testing) |
| 7 | Sign test divider | [sign](index.html#sign) |
| 8 | Matched pairs, D=X−Y, sign binomial p=.5 | [sign](index.html#sign) |
| 9 | p=P(X>Y), alternatives/tails, independent pairs | [sign](index.html#sign) |
| 10 | Factory full paired dataset | [sign](index.html#sign) |
| 11 | Region {0,10}, alpha .001953125; dbinom | [sign](index.html#sign) |
| 12 | Regions including {1,9}, then {2,8} | [sign](index.html#sign) |
| 13 | M2 rejection at chosen alpha .109375; ties removal; median null | [sign](index.html#sign) |
| 14 | DescTools SignTest S2,p.1094,CI[-26,15],median−10 | [sign](index.html#sign) |
| 15 | Signed-rank divider | [wilcoxon](index.html#wilcoxon) |
| 16 | Signs plus magnitude ranks; equal expected rank sums | [wilcoxon](index.html#wilcoxon) |
| 17 | Zero removal; tied midranks; T=min(T+,T−) | [wilcoxon](index.html#wilcoxon) |
| 18 | Directional small opposite sign rank sum; table9 reference | [wilcoxon](index.html#wilcoxon) |
| 19 | Image summary of hypotheses/statistic/rejection | [wilcoxon](index.html#wilcoxon) |
| 20 | 10 exam pairs and tied ranks | [wilcoxon](index.html#wilcoxon) |
| 21 | wilcox paired output V10.5,p.09218,CC | [wilcoxon](index.html#wilcoxon) |
| 22 | 8 blood-pressure pairs, one-sided stress higher | [wilcoxon](index.html#wilcoxon) |
| 23 | MW divider | [mann-whitney](index.html#mann-whitney) |
| 24 | Direct pairwise counting example U14 | [mann-whitney](index.html#mann-whitney) |
| 25 | Image formula U=n1n2+n1(n1+1)/2−W | [mann-whitney](index.html#mann-whitney) |
| 26 | Symmetry, support0..n1n2, one/two tails | [mann-whitney](index.html#mann-whitney) |
| 27 | Image exact CDF table n2=3,4 | [mann-whitney](index.html#mann-whitney) |
| 28 | Image summary incl independently selected samples, ties | [mann-whitney](index.html#mann-whitney) |
| 29 | Independent unequal sample R dataset incl NA; W16,p.8763 | [mann-whitney](index.html#mann-whitney) |
| 30 | Kraft-paper problem and image dataset/ranks | [mann-whitney](index.html#mann-whitney) |
| 31 | Image exact CDF table n2=10 | [mann-whitney](index.html#mann-whitney) |
| 32 | Image large-sample Z formula / one/two rejection tails | [mann-whitney](index.html#mann-whitney) |
| 33 | KW divider | [kruskal-wallis](index.html#kruskal-wallis) |
| 34 | ANOVA relationship; k groups, unequal ni; location model | [kruskal-wallis](index.html#kruskal-wallis) |
| 35 | Combined ranks, Ri,average ranks,V | [kruskal-wallis](index.html#kruskal-wallis) |
| 36 | Overall rank, H equivalent forms, chi-square k−1,ni≥5 | [kruskal-wallis](index.html#kruskal-wallis) |
| 37 | Image summary/null/alternative/H/assumptions | [kruskal-wallis](index.html#kruskal-wallis) |
| 38 | Assembly-line image raw data/ranks/sums | [kruskal-wallis](index.html#kruskal-wallis) |
| 39 | Solution H6.097,p.0474,critical5.991465; wrong printed210² | [kruskal-wallis](index.html#kruskal-wallis) |
| 40 | Campaign dataset and design | [kruskal-wallis](index.html#kruskal-wallis) |
| 41 | kruskal.test data and formula; reshape::melt | [kruskal-wallis](index.html#kruskal-wallis) |
| 42 | Runs divider | [runs](index.html#runs) |
| 43 | Random order hypotheses; stock/factory/clinical uses | [runs](index.html#runs) |
| 44 | Runs definition, sequences4 and5 runs | [runs](index.html#runs) |
| 45 | E,variance,Z | [runs](index.html#runs) |
| 46 | Hospital15-day sequence | [runs](index.html#runs) |
| 47 | Manufacturing18-item sequence | [runs](index.html#runs) |
| 48 | 20-observation plotted sequence, counts8 and12 | [runs](index.html#runs) |
| 49 | DescTools RunsTest R8,m8,n12,p.239 | [runs](index.html#runs) |
| 50 | Rank correlation divider | [spearman](index.html#spearman) |
| 51 | Teacher dataset image: judge ranks,score ranks | [spearman](index.html#spearman) |
| 52 | Question of agreement; Pearson formula as background | [pearson](index.html#pearson) |
| 53 | Spearman Pearson-of-ranks formula and no-tie simplification | [spearman](index.html#spearman) |
| 54 | Kendall concordant/discordant tau-a formula | [kendall](index.html#kendall) |
| 55 | Teacher R coefficients three methods | [spearman](index.html#spearman) |
| 56 | BMI/CRP full dataset | [spearman](index.html#spearman) |
| 57 | Applications,transform interpretation,efficiency | [conclusions](index.html#conclusions) |

## Reference documentation checked

The implementation follows the supplied lecture approach. Function behavior was checked against R/package documentation and actual execution: [R glm](https://stat.ethz.ch/R-manual/R-devel/library/stats/html/glm.html), [R wilcox.test](https://stat.ethz.ch/R-manual/R-devel/library/stats/html/wilcox.test.html), [R kruskal.test](https://stat.ethz.ch/R-manual/R-devel/library/stats/html/kruskal.test.html), and [DescTools manual](https://cran.r-project.org/web/packages/DescTools/DescTools.pdf). Explicit exact=FALSE, correct=TRUE calls preserve the lecture’s tied Wilcoxon approximations if future defaults change.
