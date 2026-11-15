# Analysis Plan (version 2)

**Normative compliance among young people: institutional anomie, procedural justice and situational action in the Istanbul ISRD-3 data**

This document sets out the analytic strategy before the revised models are run. It replaces version 1, which was written before the submission to the *...* and the reviews that followed. Version 2 changes the theoretical framing, the measurement of the three theories, the serious-offending outcome, and the treatment of clustering, missing data and age. A change log at the end records every departure from version 1 and the reason for it.

Version 1 results are already known to us. The hypotheses below are therefore not preregistered in the strict sense. Each is derived from the theory and from the ISRD-3 design documents (Marshall et al., 2013; ISRD3 Working Group, 2013), and the source of each is stated so that readers can judge this for themselves.

## 1. Theoretical framework

The framework is taken from the ISRD-3 design itself. The background paper (Marshall et al., 2013, Module 10 section, written by M. Hough) places procedural justice within a broader set of compliance theories and distinguishes two families. The first is a political-economy family, of which institutional anomie theory (IAT) is the example: economic dominance and market values weaken the capacity of non-economic institutions to transmit restraining norms. The second concerns the effect of formal social-control institutions on norms, of which procedural justice theory (PJT) is the example: fair and respectful treatment by the police builds legitimacy and, through it, compliance. The background paper treats the two families as compatible and calls for their integration. It states the key question as the relative weight of institutional behaviour (police, courts) and of underlying social and economic conditions in normative compliance.

Situational action theory (SAT) enters as the micro-level link. The background paper (Module 6 and Module 9 sections) states that personal morality and shaming, combined with norm transmission strength, allow the micro level of SAT to be linked to the macro level of IAT. In SAT, morality is act-specific and self-control matters mainly where morality does not rule an act out (Wikström & Svensson, 2010).

The study is therefore framed as an integrative test, not a contest between rival theories. It asks how the two compliance families relate to offending, alongside the individual moral and self-regulatory propensities that SAT places at the point of action, and whether each relates most clearly to the kind of offending its theory addresses.

Deterrence is not tested. ISRD-3 carries no measure of the perceived certainty or severity of sanctions. The item on police response speed (q10.2) is classed by the ISRD-3 designers as trust in police effectiveness, a component of trust in justice, and is treated here in that sense. The Turkish juvenile-justice reform is described as context in the introduction and returned to briefly in the discussion; no conclusion about sentencing or deterrence is drawn from the data.

## 2. Research questions and hypotheses

**RQ1.** How are the institutional-anomie and procedural-justice mechanisms, and the SAT propensities of morality and self-control, associated with self-reported offending among Istanbul ninth-graders?

**RQ2.** Does each mechanism relate most clearly to the type of offending its theory addresses, and do the associations differ by gender?

**RQ3.** Among young people, do procedural fairness and police effectiveness relate to legitimacy in the way found for Istanbul adults (Karakuş, 2017)?

Hypotheses (confirmed 31 October 2026, before the revised models were run):

- **H1 (IAT).** Stronger norm transmission against unethical profit-making (vignette 9.1) is associated with less offending, and the association is stronger for acquisitive than for violent offending. Source: IAT concerns instrumental crime in pursuit of material gain; vignette 9.1 was designed to capture norms about gain at others' expense ("market morality"; Marshall et al., 2013).
- **H2 (PJT, legitimacy).** Higher legitimacy is associated with less offending, and the association does not differ by offence type. Source: in PJT legitimacy is a general orientation towards legal authority, not an act-specific norm.
- **H3 (PJT, antecedents).** Procedural fairness is more strongly associated with legitimacy than perceived police effectiveness is. Source: Sunshine and Tyler (2003); tested against Karakuş (2017), who found the reverse among Istanbul adults.
- **H4 (SAT, act-specific morality).** Offence-specific shame is associated with the matching offence type: shame about shoplifting with property offending, and shame about hurting someone with violent offending. Source: SAT treats moral rules as act-specific, and the ISRD-3 designers list the shaming items as part of Wikström's morality construct.
- **H5 (SAT, interaction).** The association between self-control and offending is weaker among young people with stronger morality. Source: Wikström and Svensson (2010).
- **H6 (gender).** No directional hypothesis. Gender differences in the associations are examined as an exploratory question and reported as such.

## 3. Sample and design

We use the Turkish ISRD-3 sample (`country == 900`), collected by the Istanbul University team. The median fieldwork date (`srvdate`) is May 2017. The variable `cityid` codes four Istanbul regions (Istanbul Region 1 to 4; grade 9 n = 337, 315, 345 and 242), so the whole sample is from Istanbul. How the four regions were defined (for example, by level of deprivation or development) is to be confirmed with the Istanbul team. The Turkish sample has 2,336 respondents in grades 7 to 9, of whom 1,239 are in grade 9 (Enzmann et al., 2024, Table 1).

The procedural-justice items (Module 10) were administered to grade 9 only, so all comparative models are estimated on the grade 9 subsample. The IAT and SAT measures are also available for grades 7 and 8 and are used there in a robustness check of H1, H4 and H5.

The standard ISRD-3 design is a multi-stage cluster sample: cities selected non-randomly, all schools in the city listed, all grade 7 to 9 classes listed, and classes drawn with probability proportional to size (Enzmann et al., 2024, p. 4). The primary sampling unit is the class. Turkey is one of the countries with population weights (`p_weight`). The file holds two analytic weights, `a_weight_s` (standard grade range) and `a_weight_e` (extended range); grade 9 belongs to the standard range, so `a_weight_s` is used where an analytic weight is needed.

In grade 9 there are 47 classes in 47 schools (class size 11 to 38, median 28), so each school contributed one class and class and school clustering cannot be separated. Across grades 7 to 9 the sample contains 95 schools. The class identifier (`classid`) is used for clustering, giving 47 clusters.

The design is stratified by region × school type (`cityid` × `schtypeid`). The cross-tabulation shows exactly one value of `p_weight` in each of the 12 cells, which confirms 12 strata. Grade 9 cell sizes range from 12 to 275:

| Region | School type 1 | School type 2 | School type 3 |
|---|---|---|---|
| Istanbul Region 1 | 32 (w = 284) | 30 (w = 379) | 275 (w = 85) |
| Istanbul Region 2 | 111 (w = 92) | 21 (w = 360) | 183 (w = 139) |
| Istanbul Region 3 | 146 (w = 100) | 59 (w = 196) | 140 (w = 212) |
| Istanbul Region 4 | 72 (w = 198) | 12 (w = 448) | 158 (w = 119) |

Classes per stratum range from 1 to 10. Three strata contain a single class (Region 1 school type 1; Region 2 school type 2; Region 4 school type 2); in the survey-weighted models these are handled with the standard single-PSU adjustment (`options(survey.lonely.psu = "adjust")`). In the multilevel models, region and school type enter as two sets of main effects rather than 12 stratum dummies, because a stratum dummy for a single-class stratum would absorb that class's random intercept. The survey-weighted sensitivity models use the 12 strata, `classid` as cluster and `p_weight` as weight. What the three school types are is to be confirmed with the Istanbul team.

Class-level participation was reported as 95 of 261 selected classes across grades 7 to 9. The number of grade 9 classes selected is requested from the Istanbul team so that a grade 9 participation rate can be reported. The sampling frame, the selection of schools and classes, the student response rate and the comparison of participating and non-participating classes by socio-economic stratum are requested from the Istanbul team and will be reported in the Methods.

ISRD-3 uses city samples because its aim is theoretical explanation rather than national estimation (Marshall et al., 2015; Enzmann et al., 2024). Findings are generalised to students in the sampled classes of Istanbul, not to Türkiye.

## 4. Response integrity and screening

Unchanged from version 1. The five-indicator panel (Relevin, long-string, psychometric synonyms, Mahalanobis distance, coder's quality rating `qrating`) removes cases flagged by at least two indicators, with a coder verdict of "not usable" sufficient on its own. This removed 54 of 1,239 grade 9 cases, leaving 1,185. A further four cases that left almost every measurement item blank (24 or more missing) are removed when the scales are built, leaving 1,181. Both steps are reported.

Non-disclosure of cannabis use (`openness`) is not a deletion criterion. It is reported as a rate and used in a sensitivity analysis. The crosswise-model estimate (`crossov`) is used only at the aggregate level, to compare the directly reported prevalence of the bundled offences with an estimate that does not depend on individual disclosure. The crosswise procedure is described in the Methods, not only in the Discussion. The crosswise question bundles the same four offences and reference period as the direct comparison (shoplifting, robbery, assault with injury and burglary in the last 12 months), with the mother's birthday in January to March as the unrelated question (p = .25). The estimate is computed on the screened sample, restricted to respondents who answered the crosswise item, and the direct prevalence is computed on the same respondents. It is reported with its 95% confidence interval. Two cautions are stated: crosswise estimates are pushed towards 50 per cent by random answering, so they are an upper bound rather than a true prevalence; and if officially registered birth dates in Türkiye cluster in January, p may exceed .25, which would lower the estimate. A sensitivity calculation with p = .30 is reported. The Relevin and non-disclosure rates are reported for grade 9, the analytic sample, not for all grades.

## 5. Dependent variables

**Item source.** Offence items are taken from the dataset's own derived variables rather than rebuilt by hand. Last-year prevalence uses the `*lyp` variables, which the data producers set to 0 where lifetime prevalence is "no" (Enzmann et al., 2024, p. 9). Last-year frequency uses the outlier-adjusted `*_ia` variables (Table 3 of the Data Manual). All outcomes are built in one sourced function file so that every notebook uses identical definitions.

**Offence set.** Thirteen offences: graffiti, vandalism, shoplifting, burglary, bicycle theft, car theft, theft from a car, extortion/robbery, personal theft, weapon carrying, group fighting, assault and drug dealing. Animal cruelty, an optional ISRD-3 item, was not measured in the Istanbul sample. Illegal downloading is excluded from versatility and from the offence types because it is an online intellectual-property offence rather than the street delinquency the theories address. It is not near-universal in this sample (last-year prevalence 20.7 per cent, 8.9 per cent missing), so version 1's justification is dropped. It is modelled as a separate supplementary outcome and serves as an additional act-specific check, since the morality scale contains a matching item (`prosoc4`, how wrong it is to download illegally).

**Versatility (RQ1).** Number of the thirteen offences committed in the last year (0–13). Computed when at least ten of the thirteen items are answered; remaining blanks are treated as "not committed" in the main analysis and bounded in the sensitivity analysis.

**Offence types (RQ2).** Binary indicators of any last-year involvement:

| Type | Offences |
|---|---|
| Property | shoplifting, burglary, bicycle theft, car theft, theft from a car, personal theft |
| Violent | extortion/robbery, weapon carrying, group fighting, assault |
| Other | graffiti, vandalism, drug dealing |

Robbery is placed with violence by its use of force. The "other" group is heterogeneous and is reported descriptively but not used to test hypotheses.

**Serious offending (replaces "serious involvement").** Version 1 defined serious involvement as two or more offence types or any type committed twice. All three reviewers and the editor pointed out that this measures versatility or repetition, not severity. Version 2 uses offence severity: any last-year involvement in burglary, car theft, extortion/robbery, assault, weapon carrying or drug dealing. A frequency-based version (any of these committed three or more times, using `*_ia`) is a sensitivity check.

Coefficients from the count model and the logistic models are on different scales and are not compared in size across models (Mood, 2010). Comparisons across outcomes rely on formal tests (Section 8.4) and on average marginal effects.

## 6. Independent variables

Item wording and response scales for every construct are reported in an appendix table. Higher scores indicate more of the named construct. All multi-item scales are scored as item means under the ISRD-3 producers' rule: a score is computed only if at least two items are valid and no more than one third are missing (Enzmann et al., 2024, p. 8). This replaces the "at least half answered" rule of version 1, so that our scales and the dataset's own self-control scores follow the same rule. All variables are built in one function file (`R/build_vars.R`) called from one notebook (`03_build_variables.Rmd`), which replaces notebooks 03 and 04 of version 1.

### 6.1 Procedural justice theory (Module 10)

| Construct | Items | Notes |
|---|---|---|
| Procedural fairness | `pjresp`, `pjfair`, `pjexpl` (q10.3–10.5) | respect, fair decisions, explanation |
| Equal treatment | `pjdiscr` (q10.1) | binary: 0 = "equally" coded 1, 1 = "some worse" coded 0; "don't know" is missing |
| Trust in police effectiveness | `pjspeed` (q10.2) | response speed; trust in effectiveness, not deterrence |
| Legitimacy: obligation to obey | `pjduty` (q10.6) | 0–10 |
| Legitimacy: moral alignment | `pjattri1`–`pjattri3` (q10.7) | 1–5 |
| Legitimacy: lawfulness | `pjbribes_r` (q10.8, reversed) | 0–10 |

The factor structure of legitimacy is tested before scoring. The primary legitimacy measure combines all three dimensions: obligation to obey, moral alignment and lawfulness. The justification is the ISRD-3 design itself. Module 10 was adapted from the European Social Survey "Trust in Justice" module, and the background paper classes all three items as institutional legitimacy (Marshall et al., 2013, Table 10), following the three-part structure of Jackson et al. (2012). Because some authors treat lawfulness as an antecedent of legitimacy rather than a component (Tankebe, 2013), a sensitivity model removes it from the composite. Items on different response scales are standardised before averaging.

### 6.2 Institutional anomie theory (Module 9)

Norm transmission strength (NTS) is built as the ISRD-3 designers specified: subjective norms of each informant multiplied by the respondent's bond to that informant (Marshall et al., 2013, Module 9 section).

| Informant | Subjective norms, vignette 9.1 (profit-making) | Subjective norms, vignette 9.3 (theft) | Bond |
|---|---|---|---|
| Parents | `profsnmo`, `profsnfa` (averaged) | `shopsnmo`, `shopsnfa` (averaged) | family bond, q2.1 (`fambond1`–`fambond4`) |
| Favourite teacher | `profsnte` | `shopsnte` | teacher bond, q3.2 and q3.3 (`teabond1`, `teabond2`) |
| Best friend | `profsnfr` | `shopsnfr` | friend bond, q5.8 and q5.9 (`frdbond1`, `frdbond2`) |
| Classmates | `profsncm` | `shopsncm` | no bond item; subjective norms only |
| Neighbourhood peers | `profsnpe` | `shopsnpe` | no bond item; subjective norms only |

Subjective norms run from 1 (would admire me) to 5 (would criticise me). Each norm score and each bond score is rescaled to 0–1 (POMP) before multiplication, so that the product is 0–1 and comparable across informants.

The NTS score for each vignette is the mean of the three bonded informants (parents, favourite teacher, best friend). Classmates' and neighbourhood peers' subjective norms have no matching bond item; they are kept as separate scores and used descriptively and in a sensitivity model. Informant-specific NTS scores are reported descriptively.

The primary IAT measure is NTS for vignette 9.1, because it concerns unethical but legal gain at another's expense and was designed to capture market morality. NTS for vignette 9.3 (theft) is analysed separately as a secondary measure, because norms against theft are also predicted by social learning and social control theories and cannot be read as specific to IAT.

The bonding items are six-point scales (teacher and friend) and the subjective-norm items five-point scales; codes 97, 98 and 99 are already missing.

Friend bond (`frdbond1`, `frdbond2`) is missing for about 9 per cent of grade 9 respondents. Of these, 70 have no group of friends (q5.7, `groupfr`), so the item does not apply; 35 have a group of friends but did not answer; 6 are missing on both. For the 70 without a group of friends, friend bond is set to its minimum (0 on the POMP scale), on the reasoning that without a friend group there is no transmission from friends, and an indicator for having no friend group is added. A sensitivity model excludes these 70 cases. The remaining missing values are multiply imputed. The friend vignette item (`profsnfr`, `shopsnfr`) refers to the best friend, whereas the bond items refer to the friend or group of friends; this mismatch is noted in the Methods.

To reflect the institutional level of the theory, NTS is also aggregated to the class mean and entered as a class-level predictor alongside the individual score (within/between decomposition). With 47 classes this is feasible, but class-level estimates will be imprecise and are reported as such.

The intention items `profint` (q9.2, "Can you imagine actually doing this?") and `shopint` (q9.4, "... if you were certain of not getting caught?") are not used as predictors. They are examined descriptively as indicators of willingness to profit at others' expense.

Because a product term is uninterpretable without its components, a sensitivity model enters subjective norms, bond and their interaction separately.

### 6.3 Situational action theory (Module 6)

**Morality** (`prosoc1`–`prosoc8`, q6.1; 1 = not wrong at all to 4 = very wrong). The full eight-item scale is used in the theory-block models and in the morality × self-control interaction (H5). The scale contains items on specific acts (`prosoc5` stealing from a shop, `prosoc6` burglary, `prosoc7` hitting to hurt, `prosoc8` using force to get money), but two-item subscales are too short to carry a hypothesis test. The act-specific test (H4) therefore rests on the shame items, and the limits of the morality scale for act-specific analysis are stated among the limitations.

**Shame** (q6.2–6.4; no / a little / very much, if best friend, teacher or parents found out). Three scores: shame about shoplifting (q6.2; `shamfrd1`, `shamtea1`, `shampar1`), shame about hurting someone (q6.3; `shamfrd2`, `shamtea2`, `shampar2`), and shame about arrest (q6.4; `shamfrd3`, `shamtea3`, `shampar3`). The ISRD-3 designers list these items as part of Wikström's morality construct (Marshall et al., 2013, Module 6 section).

**Self-control** (`selfc01`–`selfc09`, q6.5). The dataset's own scale score `selfc` and its three subscales are used: impulsivity (`lselfcim`), risk-taking (`lselfcrt`) and self-centredness (`lselfcsc`). These are POMP scores built with the producers' "minimum 2 valid, maximum 1/3 missing" rule (Enzmann et al., 2024, p. 8), and are converted to z-scores before modelling. The subscales are scored as low self-control (higher = less self-control), the reverse of `selfc`; they are reversed before modelling so that all self-control measures run in the same direction. The ISRD-3 scale has no temper items (Marshall et al., 2013, Table 6).

### 6.4 Controls

Sex (`male`), relative family affluence (`deprfam`), school bond (`schbond1`–`schbond4`) and delinquent peers (`delpdr`, `delpsl`, `delpbu`, `delpex`, `delpas`).

Age is not used as a control. The Data Manual advises against it, because with classes as sampling units age is confounded with grade repetition, achievement and problem behaviour (Enzmann et al., 2024, pp. 7–8). Within a single grade, older age mainly indicates repetition. An indicator of being over-age for grade 9 is examined in a sensitivity model.

The delinquent-peer score requires at least four of the five items answered; it is no longer computed with blanks counted as "no". Because peers are part of criminogenic exposure in SAT and a mediator in social learning theory, the main models are reported with and without the peer control.

Family bond enters the models through the parental NTS product; it is not also entered as a separate control except in the sensitivity model described in 6.2.

## 7. Measurement

Each construct is tested by confirmatory factor analysis (WLSMV for ordinal items) before scoring. Fit indices, loadings and composite reliability (ω) are reported for every scale. Scale scores, not latent factors, are used in the outcome models. The reasons are the ceiling effect on the morality items, the multidimensionality of the self-control scale, and the instability of latent models when the sample is split by gender. Reliability is also reported separately for boys and girls.

Results of the measurement models (04_measurement):

- Self-control: one factor fits poorly (RMSEA .183); three factors (impulsivity, risk-taking, self-centredness) fit well (CFI .997, RMSEA .033; factor correlations .54–.66). A second-order factor over three first-order factors is statistically equivalent to the three-factor model, which justifies the general score `SC`; the subscales are used in sensitivity models.
- Legitimacy: five items fit well (CFI .996, RMSEA .058); four items without lawfulness fit slightly better (RMSEA .023). The five-item composite is retained, with lawfulness removed in sensitivity.
- Morality: one factor fits moderately (CFI .941, RMSEA .104), reflecting the ceiling effect and the mix of minor and serious acts; reported as a limitation of the latent structure, not a bar to the scale score.
- Shame: three offence-specific factors fit better than one (RMSEA .109 vs .140; factor correlations .74–.84). Vignettes: two factors fit better than one (RMSEA .145 vs .203; correlation .59), supporting separate profit-making and theft measures. Because the same informants recur across blocks, models with residual correlations for the same informant (and for mother and father in the vignettes) were estimated. For shame this resolves the misfit (CFI .996, RMSEA .046, SRMR .031), and the factor correlations fall to .67–.71, so the three shame scores are distinct enough to carry H4. For the vignettes fit improves only slightly (CFI .994, RMSEA .143, SRMR .079; profit–theft correlation .56). A four-factor model separating adult informants (mother, father, teacher) from peer informants (best friend, classmates, neighbourhood peers) within each vignette is tested, because IAT locates norm transmission in non-economic institutions (family, school) rather than in peers. The four-factor model fits clearly better (CFI .999, RMSEA .072, SRMR .033, against RMSEA .143 for two factors). Adult and peer norms correlate .86 for profit-making and .80 for theft: closely related but distinct. An institutional NTS (parents and teacher only; `NTS_prof_inst`, `NTS_shop_inst`, with class means) is therefore built alongside the three-informant NTS. **Decision:** the institutional NTS for vignette 9.1 (`NTS_prof_inst`) is the primary IAT measure, because IAT locates norm transmission in non-economic institutions (family, school) and the CFA separates adult from peer norms. Its cost is higher missingness (9.0% vs 2.0%), handled by multiple imputation. The three-informant NTS (`NTS_prof`) and the peers' subjective norms (`SN_prof_cm`, `SN_prof_pe`) are used in sensitivity models.
- Full model: CFI .982, RMSEA .057, SRMR .074. All HTMT values are below .85 (highest: legitimacy–procedural fairness .72; shame shoplifting–shame hurting .71), supporting discriminant validity. Subjective norms about profit-making correlate weakly with all other constructs (.08–.32).
- Latent factors carry an `f_` prefix in the code to avoid clashing with scale-score names. HTMT is computed from the polychoric correlations of the full model rather than from listwise data, because listwise deletion left an empty category in `prosoc3`.

## 8. Analytic strategy

### 8.1 Descriptive analysis

Distributions, missingness for every variable, prevalence of each offence type by gender, intra-class correlations of all outcomes and of the NTS measures, and bivariate correlations among the predictors.

Results (05_descriptives):

- ICCs are low for most variables (.01–.07), but high for property offending (.19, latent scale) and illegal downloading (.19). Property offending is concentrated in some classes, so the multilevel specification matters most for that model. The ICC for "other" offending is zero. NTS for profit-making has an ICC of .06, so there is some between-class variation for the institutional level of IAT.
- Boys report more property (10.3% vs 3.7%), violent (29.7% vs 14.8%), serious (21.5% vs 7.2%) and downloading (35.0% vs 10.4%) offending; "other" offending is similar (23.6% vs 24.5%). Only 24 girls report property offending, which confirms that sex × offence type cannot be modelled jointly.
- The highest predictor correlations are NTS profit–theft (.64; never in the same model), shame shoplifting–arrest (.60) and legitimacy–procedural fairness (.54). No collinearity problem is expected. Family affluence (`deprfam`) is almost uncorrelated with every predictor.
- 1,063 cases (90.0%) are complete on the model variables; 86 miss one and 32 miss two or more. Incomplete cases report less offending (mean versatility 0.53 vs 0.72), so data are not missing completely at random; multiple imputation with the outcomes in the imputation model is required. Missing family bond coincides with blank father and mother items (50 and 49 cases), which may reflect family structure; this is checked against household composition (q1.6).

### 8.2 Model family and clustering

Versatility is modelled by negative binomial regression, and the binary outcomes by logistic regression. All models include a random intercept for class (`classid`). The class-level NTS mean enters as a level-2 predictor. A sensitivity version re-estimates the main models as survey-weighted single-level models with `p_weight`, clustering on `classid`. Continuous predictors are standardised. Effects are reported as incidence rate ratios or odds ratios with 95% confidence intervals, average marginal effects, and predicted values at the 10th and 90th percentiles of each predictor.

### 8.3 RQ1: contribution of each theory

Models are built in blocks. Controls: sex, family affluence, school bond, delinquent peers, region, school type. PJT block: legitimacy, procedural fairness, equal treatment, effectiveness. IAT block: institutional NTS 9.1, decomposed into the within-class deviation and the class mean. SAT block: morality, shame about shoplifting, shame about hurting someone, self-control (shame about arrest is used in sensitivity only, because it is not act-specific). Each block's contribution is assessed two ways: its total contribution (controls + block against controls) and its unique contribution (full model against the full model without the block). Both are likelihood-ratio tests computed in each imputed dataset and pooled with the D2 rule, alongside the mean change in AIC. Relative importance is not inferred from the size of standardised coefficients. Models are estimated with `glmmTMB` (negative binomial type 2 for versatility; binomial for the binary outcomes), and coefficients are pooled across imputations with Rubin's rules. Complete-case estimates are reported alongside.

### 8.4 RQ2: offence type and gender

Offence type is analysed in a stacked model. Each respondent contributes one row for property and one for violent offending. The model has a random intercept for respondent and for class, and interactions between each mechanism and offence type. The mechanism × type terms test H1, H2 and H4 directly. Each type is also modelled separately: the property model (77 events) by penalised Firth logistic regression (Firth, 1993), and the violent model by standard logistic regression.

Implementation (09_models_RQ2): in the stacked model, all individual-level variables (theory terms, sex, family affluence, school bond, delinquent peers) interact with offence type, while region, school type and class-level NTS are shared across types, to avoid separation in strata with few property offenders. Type-specific odds ratios are obtained as pooled linear combinations. The supplementary downloading model adds the matching morality item (`prosoc4`) and replaces the full morality scale with a seven-item version without that item.

First-run results (20 imputations) and resulting changes. H4 is supported for shame about shoplifting: property OR 0.70 per SD (p = .02), violent 1.19 (n.s.), difference p = .002. For shame about hurting the pattern is in the predicted direction (violent OR 0.60, p < .001; property 0.90, n.s.) but the difference is borderline (p = .058). Self-control relates to violent (OR 0.57) but not property offending (0.87), difference p = .04; morality relates to property (OR 0.70) but not violent offending (0.97), difference p = .067. H2: legitimacy does not differ by type (p = .48), but is not significant for either type. H1 at the individual level is not supported (within-class NTS: property 1.13, violent 0.90, difference p = .23). However, the class-level NTS is strongly associated with property offending in the separate models (OR 0.55, p < .001; Firth 0.56), consistent with IAT's institutional claim. In the first run the class-level term was shared across types, so H1 was not tested at that level. Two changes follow: class-level NTS is now interacted with offence type in the stacked model, and a leave-one-class-out check tests whether the class-level association depends on any single class (47 classes; property ICC .19). Because the class mean may also reflect class composition, it is interpreted as an association with the normative climate of the class, not as an institutional effect. Gender: the nine mechanism × sex interactions are jointly non-significant (D2 p = .51, ΔAIC +9.5).

Second-run results (class-level NTS by type; corrected gender output; seven-item morality in the downloading model). H1 is supported at the class level: class-level institutional NTS is associated with property offending (OR 0.62 per SD, p = .006) but not violent offending (0.92), difference p = .029. Leaving out each of the 47 classes in turn, the property coefficient stays between −0.71 and −0.58 with p ≤ .001 in every run, so no single class drives it. Within-class NTS still shows no type difference (p = .28). H4: both differences are now significant, shame about shoplifting (p = .002) and shame about hurting (p = .048). Self-control: difference p = .034; morality: p = .053. H6: jointly non-significant (D2 p = .51). One of nine single interactions has p < .05 (equal treatment × sex, p = .038), which does not survive a false-discovery-rate correction across the nine tests and is reported as such. Minimum detectable differences are 0.27–0.33 on the log scale (0.62 for equal treatment), so only fairly large sex differences in slopes could have been detected. Downloading: the matching morality item is strongly protective (OR 0.29 per SD, p < .001). With that item in the model, the seven-item morality scale turns positive (OR 1.41), a suppression effect from the shared variance of the two measures, which is reported but not interpreted substantively.

Random intercepts: the random intercept is for class (47 classes, 11–38 students), not for region; region (four levels) and school type are fixed effects because four or three levels are too few to estimate a variance. Strata with a single class do not affect the class random intercept; small classes are shrunk more towards the overall mean. The agreement between the multilevel and single-level Firth estimates for property offending indicates that the random intercept is not driving the results.

Gender is analysed by adding mechanism × sex interactions to the versatility model. Interactions are interpreted through average marginal effects by sex, not through the product terms alone. Non-significant interactions are reported as a failure to detect a difference, not as evidence of equality. The minimum detectable difference (2.8 × the pooled standard error of each interaction, 80% power at α = .05) is reported. The interactions are tested jointly (pooled likelihood-ratio test, D2) and individually. Average marginal effects by sex are on the scale of the expected number of offence types per SD of the predictor, at the population level (random effects set to zero).

### 8.5 RQ3: antecedents of legitimacy

A multilevel linear model regresses legitimacy on procedural fairness, effectiveness, equal treatment and the controls (H3). H3 is tested formally as the pooled difference between the fairness and effectiveness coefficients (both per SD). Respondents whose legitimacy score was imputed are excluded from this model, because legitimacy is the outcome here. The indirect association of fairness and effectiveness with offending through legitimacy is the product of the path to legitimacy and the path from legitimacy to offending (controls + PJT block model, log scale per SD), averaged across imputations, with class-level bootstrap intervals (200 replicates, one random imputation per replicate). It is described as a statistical decomposition, not as causal mediation.

### 8.6 RQ1 and SAT: morality × self-control

The morality × self-control interaction (H5) is added to the versatility and offence-type models and interpreted through marginal effects of self-control across the range of morality.

### 8.6a RQ1 results (07_models_RQ1)

Imputed models n = 1,169; complete cases n = 996; the two agree closely. Entered alone with the controls, each theory block improves fit for versatility: PJT (D2 p = .002, ΔAIC −12; legitimacy IRR 0.84 per SD), IAT (p = .001, ΔAIC −12; within-class institutional NTS IRR 0.83; class mean not significant) and SAT (p < .001, ΔAIC −114). In the full model only SAT adds a unique contribution (ΔAIC −92); the unique contributions of PJT (p = .20) and IAT (p = .50) are not significant. Full-model IRRs per SD: self-control 0.74, shame about hurting 0.78, morality 0.89; shame about shoplifting null. Serious offending shows the same pattern; legitimacy is borderline in the full model (OR 0.78, p = .11 imputed; p = .04 complete case). H5 is not supported (morality × self-control p = .22 versatility, .40 serious). Delinquent peers and male sex are the strongest controls.

### 8.6b Supplementary: overlap of PJT and IAT with SAT (KHB decomposition)

Added after the RQ1 results, and labelled as supplementary. Because the PJT and IAT associations disappear once the SAT block is entered, we quantify how much of each PJT and IAT coefficient overlaps with the SAT block. The KHB method (Karlson, Holm & Breen, 2012) is used because coefficients from nonlinear models fitted with and without additional variables are on different scales; KHB compares the reduced and full models on the same scale by entering the residualised SAT variables in the reduced model. For each PJT and IAT variable it reports the total coefficient, the direct coefficient, their difference, the percentage overlap, and the part of the difference attributable to each SAT variable. It is run in each imputed dataset and averaged; confidence intervals come from a class-level bootstrap (200 replicates, one randomly drawn imputation per replicate). The result is described as a statistical decomposition of overlapping associations. In line with SAT's "causes of the causes" argument it is consistent with, but cannot show, that the compliance families relate to offending through individual moral propensities; the design is cross-sectional. Percentages are interpreted only where the total coefficient is clearly different from zero.

Results (08_KHB_overlap; coefficients on the log scale per SD; bootstrap 95% intervals). Within-class institutional NTS: total −0.165, direct −0.054 for versatility, so 67% of the association overlaps with SAT (difference −0.111, CI −0.155 to −0.067); for serious offending 77% (difference −0.151, CI −0.267 to −0.061). The overlap runs mainly through self-control (−0.059 and −0.092) and shame about hurting (−0.038 and −0.061), with little through morality and none through shame about shoplifting. Legitimacy: total −0.166, direct −0.100 for versatility, 39% overlap (difference −0.066, CI −0.105 to −0.027); for serious offending 25% (difference −0.085, CI −0.166 to −0.027), leaving a direct coefficient of −0.251. Legitimacy's overlap runs mainly through shame about hurting and self-control. For procedural fairness, equal treatment, effectiveness and class-level NTS the total coefficients are close to zero, so their percentages are not interpreted. Interpretive caution: because NTS is norms × family or teacher bond, and family bond correlates .35 with self-control, the overlap with self-control may come from the bonding component rather than from the transmitted norms; a sensitivity decomposition enters norms and bond separately.

### 8.7 Missing data

Missing values on predictors and controls are handled by multiple imputation by chained equations (`mice`; 20 imputations, 20 iterations; predictive mean matching for continuous variables, logistic regression for binary ones). Scale scores, not items, are imputed. The imputation model includes all analysis and sensitivity variables, the outcomes, family bond, the non-disclosure marker, region and school type, and the observed class means of NTS and offending as auxiliary variables to carry class-level information (a single-level imputation with class aggregates, chosen over a two-level model given 47 clusters and low ICCs). Outcomes are imputed so that they can inform the imputation, but cases with a missing outcome are dropped from the models of that outcome afterwards (multiple imputation then deletion; von Hippel, 2007). Class means and standardisation are recomputed within each imputed dataset. Results are compared with complete-case estimates. The fraction of missing information reaches .33–.42 for legitimacy, above what 20 imputations handle comfortably (the rule of thumb is at least 100 × FMI imputations; von Hippel, 2020). The development runs use 20 imputations; the final reported results use 50. Missingness patterns are described, and their association with offending and sex is tested.

## 9. Robustness and sensitivity

1. Blank offence items treated as "not committed" (main) and as "committed" (upper bound).
2. Exclusion of non-disclosers (`openness`).
3. Re-inclusion of the 54 screened cases.
4. Models without the delinquent-peer control.
5. Survey-weighted single-level models in place of multilevel models.
6. Frequency-based serious offending using `*_ia`.
7. NTS components entered separately (norms, bond, interaction).
8. Lawfulness inside versus outside the legitimacy composite.
9. Over-age-for-grade indicator.
10. Grades 7 to 9 for the IAT and SAT hypotheses (without the PJT block).
11. E-values for the main associations (VanderWeele & Ding, 2017), reported as a guide to sensitivity, not as proof of robustness.

## 10. Limitations to be stated

Cross-sectional design: offending refers to the past twelve months, while morality, legitimacy, norms and bonds are measured at the time of the survey and may have changed after offending or police contact; the peer items have no matching reference period. No measure of perceived sanction risk, so deterrence is not tested. Single city and school-based sample, which excludes young people out of school or in custody, who are likely to be the most serious offenders. Low class participation. Data collected in 2017, nine years before the reform debate. Act-specific morality rests on the shame items only, because the morality scale has at most two items for any offence type. Animal cruelty was not measured in Istanbul.

## 11. Decision log

**Settled.** Hypotheses H1–H6. Grade 9 analytic sample. Framing taken from the ISRD-3 compliance framework, with SAT as the micro link. NTS built as norms × bond. Profit-making vignette as the primary IAT measure. Shame items added to SAT. Dataset-derived `*lyp`, `*_ia` and self-control scores used. Animal cruelty not measured in Istanbul. Illegal downloading as a separate supplementary outcome. Serious-offending offence list. Legitimacy composite of all three dimensions, with lawfulness removed in sensitivity. H4 tested with shame items; full morality scale elsewhere. Strata confirmed as region × school type (12 strata). Age dropped as a control. Clustering on `classid`. Multiple imputation. Friend bond set to minimum for respondents without a friend group, with indicator and sensitivity model. Sample confirmed as four Istanbul regions. Stacked model for offence-type differences. Firth regression for property offending. No deterrence conclusion.

**Open.** Definition of the four Istanbul regions and of the three school types (Istanbul team). Number of grade 9 classes selected (Istanbul team). Number of classes per stratum. Source of the missing family-bond scores (6.2 per cent).

## 12. Change log from version 1

| Area | Version 1 | Version 2 | Reason |
|---|---|---|---|
| Framing | Bottoms's typology; three parallel "normative-compliance theories" against deterrence | ISRD-3 compliance framework (Hough, in Marshall et al., 2013); integrative test; SAT as micro link | Reviewer 2 and editor: theories not competing, rationale undeveloped |
| Hypotheses | Research questions only | H1–H6 derived from theory and design documents | Editor: no rationale for variation by gender or offence type |
| IAT measure | Average of subjective norms across both vignettes | NTS = norms × bond, by informant; profit vignette primary; class-level aggregate | Reviewers 1–3: norm transmission not specific to IAT; macro–micro step unjustified |
| SAT measure | Morality and self-control scales | Plus offence-specific shame items, self-control subscales, morality × self-control | Reviewer 3: not a test of SAT; content overlap |
| PJT | Legitimacy only; procedural justice not modelled | Fairness and effectiveness → legitimacy → offending | Reviewer 1: PJ–legitimacy relationship unclear |
| Effectiveness item | "Instrumental, deterrence-facing" covariate | Trust in police effectiveness | All reviewers: not a deterrence measure |
| Serious outcome | Two or more types or repetition | Offence severity | All reviewers and editor |
| Offence items | Rebuilt by hand from `*lyi`, in five places | Dataset `*lyp` and `*_ia`, one function file | Consistency; outlier treatment |
| Animal cruelty | In "other" type only | Excluded throughout | Consistency |
| Age | Continuous control | Dropped; over-age indicator in sensitivity | Data Manual pp. 7–8 |
| Delinquent peers | Blanks counted as 0 | Minimum four of five items; with/without models | Hidden imputation |
| Clustering | None | Random intercept for class; weighted sensitivity | Reviewers 1–3 |
| Missing data | Listwise deletion | Multiple imputation | Reviewer 1 |
| Cross-type comparison | Visual comparison of separate logits | Stacked model with interaction tests; Firth for property | Reviewer 1; low events per variable |
| Gender | Product terms; "operate alike" | Marginal effects; failure to detect, not equality | Reviewer 1 |
| Policy | Deterrence verdict on the reform | Context only; no deterrence conclusion | All reviewers and editor |

## References

Enzmann, D., Marshall, I. H., Hough, M., Killias, M., Kivivuori, J., & Steketee, M. (2024). *Data manual ISRD3 (dataset version 1.0)*. University of Hamburg.

Firth, D. (1993). Bias reduction of maximum likelihood estimates. *Biometrika, 80*(1), 27–38.

ISRD3 Working Group. (2013). *Questionnaire ISRD3: Standard student questionnaire* (ISRD3 Technical Report Series #2).

Karlson, K. B., Holm, A., & Breen, R. (2012). Comparing regression coefficients between same-sample nested models using logit and probit: A new method. *Sociological Methodology, 42*(1), 286–313.

Jackson, J., Bradford, B., Hough, M., Myhill, A., Quinton, P., & Tyler, T. R. (2012). Why do people comply with the law? Legitimacy and the influence of legal institutions. *British Journal of Criminology, 52*(6), 1051–1071.

Karakuş, Ö. (2017). Instrumental and normative pathways to legitimacy and public cooperation with the police in Turkey. *Justice Quarterly, 34*(1), 25–54.

Marshall, I. H., Enzmann, D., Hough, M., Killias, M., Kivivuori, J., & Steketee, M. (2013). *International Self-Report Delinquency Questionnaire 3 (ISRD-3): Background paper to explain ISRD2–ISRD3 changes* (ISRD3 Technical Report Series #1).

Marshall, I. H., Enzmann, D., Hough, M., Killias, M., Kivivuori, J., & Steketee, M. (2015). *Youth victimization and reporting to police: First results from the third round of the International Self-Report Delinquency Study (ISRD3)* (ISRD3 Technical Report Series #3).

Mood, C. (2010). Logistic regression: Why we cannot do what we think we can do, and what we can do about it. *European Sociological Review, 26*(1), 67–82.

Sunshine, J., & Tyler, T. R. (2003). The role of procedural justice and legitimacy in shaping public support for policing. *Law & Society Review, 37*(3), 513–548.

Tankebe, J. (2013). Viewing things differently: The dimensions of public perceptions of police legitimacy. *Criminology, 51*(1), 103–135.

von Hippel, P. T. (2020). How many imputations do you need? A two-stage calculation using a quadratic rule. *Sociological Methods & Research, 49*(3), 699–718.

von Hippel, P. T. (2007). Regression with missing Ys: An improved strategy for analyzing multiply imputed data. *Sociological Methodology, 37*(1), 83–117.

VanderWeele, T. J., & Ding, P. (2017). Sensitivity analysis in observational research: Introducing the E-value. *Annals of Internal Medicine, 167*(4), 268–274.

Wikström, P.-O. H., & Svensson, R. (2010). When does self-control matter? The interaction between morality and self-control in crime causation. *European Journal of Criminology, 7*(5), 395–410.

*Retained from version 1 and still to be cited in the Methods:* Curran (2016); Edwards (2019); Meade and Craig (2012); MacCallum et al. (2002); Rhemtulla et al. (2012); Enzmann et al. (2018); Wikström et al. (2012).
