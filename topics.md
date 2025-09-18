# Report Topics

## Intro
- What is fairness (VERY brief + reference)
- What dataset are we using (add some images)
  Show the basic statistic (distribution of `age_range` and patient gender)
- Recap of the key concepts
  - three criteria of fairness assessment
  - evaluation metrics for the criteria
  - ROC curves
  give a very brief coverage of this
- Disease label: pneumothorax

## Prediction (Baseline)
- Describe the "default" prediction (the pretrained model / loaded results)
- Describe the RESULTS on the test set BEFORE mitigation + ROC curve
- Discussion from the notebook:
  - What do you see from the metrics and the ROC curve?
  - Measure and describe the fairness wrt the 3 criteria we learned from class
  - (Mention any trade-off between accuracy and fairness)

## Mitigation
- Small introduction to the Threshold Optimizer (why/how it works, 2–3 sentences max)
- Show the new threshold function (from the interpolation dict)
- Compare the results:
  - Metrics & ROC after mitigation
  - Does this model seem fair to you?
  - Hint: After optimization, accuracy (or other metrics) may decrease overall but balance across groups may improve
  - Do you think this is an acceptable trade-off?

## Fairness in Presence of Label Noise
- Distortion setup: how labels were modified (healthy -> diseased for 30% of males)
- **Diagnosis before mitigation** with distorted labels: how does bias appear?
- **Mitigation under distorted labels**: re-run ThresholdOptimizer, show metrics/ROC
- **Discussion:**
  - Did mitigation improve fairness wrt distorted labels?
  - What happens if you evaluate mitigated predictions against the *true* labels?
  - Is the algorithm “actually fair,” or only fair under biased labels?
  - Broader lesson: pitfalls of fairness evaluation under noisy or biased ground truth

## Conclusion
- Summarize key takeaways (1–2 paragraphs)
    - Main insight: fairness metrics depend heavily on the correctess of labels (
    or at least this is what I think we are going to discover)

