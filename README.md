# Attention
Tracking Wikipedia daily pageview trend, and automatically post on X (Twitter).

Feel free to check out the deployed [Project's GitHub Page](https://anonym-g.github.io/Attention).

## Project structure:

```
Attention/
├── .github/
│   └── workflows/
│       └── daily_report.yml      # GitHub Action for daily execution
├── data/
│   └── *.json                    # Cache for daily top articles data
├── docs/
│   ├── css/
│   │   ├── style.css             # Main stylesheet for the visualization page
│   │   └── variables.css         # CSS custom properties (colors, fonts, etc.)
│   ├── data/
│   │   └── history_*.json        # Processed historical data for animations
│   ├── js/
│   │   ├── app.js                # Main application entry point, initializes the app
│   │   ├── constants.js          # Global constants for the frontend animation
│   │   ├── data_loader.js        # Handles fetching and loading of data files
│   │   ├── render.js             # Core animation loop and DOM rendering logic
│   │   ├── state.js              # Global state management for the visualization
│   │   ├── ui.js                 # UI event handlers and layout-related functions
│   │   └── utils.js              # Frontend utility functions (calculations, color generation)
│   ├── config.json               # Frontend configuration (e.g., color thresholds)
│   └── index.html                # The HTML page that renders the animation
├── pictures/
│   └── YYYY-MM-DD/
│       └── lang_code/*.png       # Daily screenshots for tweets
├── src/
│   ├── animator.py               # Renders the video using Playwright and FFmpeg
│   ├── config.py                 # Main project configuration
│   ├── main.py                   # Main script: orchestrates fetching, rendering, and posting
│   ├── twitter_client.py         # Handles X (Twitter) API interactions
│   ├── utils.py                  # Utility functions (file handling, cleanup)
│   ├── wiki_api.py               # Fetches data from Wikimedia APIs
│   └── test_video_gen.py         # Standalone script for testing video generation
├── videos/
│   └── YYYY-MM-DD/
│       └── lang_code/*.mp4       # Daily video segments and final outputs
├── requirements.txt              # Python dependencies
└── README.md
```

## Tweet List

#### 2025-11-19: https://x.com/trailblaziger/status/1991369684428755293
#### 2025-11-20: https://x.com/trailblaziger/status/1991704915681378329
#### 2025-11-21: https://x.com/trailblaziger/status/1992065689515954568
#### 2025-11-22: https://x.com/trailblaziger/status/1992433847783313800
#### 2025-11-23: https://x.com/trailblaziger/status/1992795370259456427
#### 2025-11-24: https://x.com/trailblaziger/status/1993155557939724576
#### 2025-11-25: https://x.com/trailblaziger/status/1993517960477220997
#### 2025-11-26: https://x.com/trailblaziger/status/1993879969034846255
#### 2025-11-27: https://x.com/trailblaziger/status/1994242524610007403
#### 2025-11-30: https://x.com/trailblaziger/status/1995392930954035418
#### 2025-12-01: https://x.com/trailblaziger/status/1995719546930635248
#### 2025-12-02: https://x.com/trailblaziger/status/1996081153841782998
#### 2025-12-03: https://x.com/trailblaziger/status/1996444567369920673
#### 2025-12-04: https://x.com/trailblaziger/status/1996806717758128618
#### 2025-12-05: https://x.com/trailblaziger/status/1997167039425708117
#### 2025-12-06: https://x.com/trailblaziger/status/1997532463455756675
#### 2025-12-07: https://x.com/trailblaziger/status/1997894778336256410
#### 2025-12-08: https://x.com/trailblaziger/status/1998256061451759809
#### 2025-12-09: https://x.com/trailblaziger/status/1998620039621058972
#### 2025-12-10: https://x.com/trailblaziger/status/1998982961899663485
#### 2025-12-11: https://x.com/trailblaziger/status/1999345335915741188
#### 2025-12-12: https://x.com/trailblaziger/status/1999705330628927589
#### 2025-12-13: https://x.com/trailblaziger/status/2000070722031636826
#### 2025-12-14: https://x.com/trailblaziger/status/2000434127837827296
#### 2025-12-15: https://x.com/trailblaziger/status/2000794932663967822
#### 2025-12-16: https://x.com/trailblaziger/status/2001156525532876901
#### 2025-12-17: https://x.com/trailblaziger/status/2001519364332491192
#### 2025-12-18: https://x.com/trailblaziger/status/2001881847748301104
#### 2025-12-19: https://x.com/trailblaziger/status/2002242503316242469
#### 2025-12-20: https://x.com/trailblaziger/status/2002608178958049490
#### 2025-12-21: https://x.com/trailblaziger/status/2002970708578595199
#### 2025-12-22: https://x.com/trailblaziger/status/2003332552774299796
#### 2025-12-23: https://x.com/trailblaziger/status/2003694460656398528
#### 2025-12-24: https://x.com/trailblaziger/status/2004057326290972878
#### 2025-12-25: https://x.com/trailblaziger/status/2004419110327681142
#### 2025-12-27: https://x.com/trailblaziger/status/2005146296227655902
#### 2026-01-04: https://x.com/trailblaziger/status/2008049314359025934
#### 2026-01-05: https://x.com/trailblaziger/status/2008406573740167286
#### 2026-01-06: https://x.com/trailblaziger/status/2008769280247001490
#### 2026-01-07: https://x.com/trailblaziger/status/2009131639167721699
#### 2026-01-08: https://x.com/trailblaziger/status/2009494269220819190
#### 2026-01-09: https://x.com/trailblaziger/status/2009855111066202168
#### 2026-01-10: https://x.com/trailblaziger/status/2010221086583988309
#### 2026-01-11: https://x.com/trailblaziger/status/2010583836053172313
#### 2026-01-12: https://x.com/trailblaziger/status/2010944089165058357
#### 2026-01-13: https://x.com/trailblaziger/status/2011308149609771063
#### 2026-01-14: https://x.com/trailblaziger/status/2011668691910279258
#### 2026-01-15: https://x.com/trailblaziger/status/2012031428629053833
#### 2026-01-16: https://x.com/trailblaziger/status/2012391562907689255
#### 2026-01-17: https://x.com/trailblaziger/status/2012756624817922199
#### 2026-01-18: https://x.com/trailblaziger/status/2013120707450868117
#### 2026-01-19: https://x.com/trailblaziger/status/2013481679453855880
#### 2026-01-20: https://x.com/trailblaziger/status/2013843636606148803
#### 2026-01-21: https://x.com/trailblaziger/status/2014207210256306513
#### 2026-01-22: https://x.com/trailblaziger/status/2014568707880599814
#### 2026-01-23: https://x.com/trailblaziger/status/2014929283760734245
#### 2026-01-24: https://x.com/trailblaziger/status/2015295452451631477
#### 2026-01-25: https://x.com/trailblaziger/status/2015659258918916569
#### 2026-01-26: https://x.com/trailblaziger/status/2016018938535018837
#### 2026-01-27: https://x.com/trailblaziger/status/2016380709661815144
#### 2026-01-28: https://x.com/trailblaziger/status/2016749538405474559
#### 2026-01-29: https://x.com/trailblaziger/status/2017115811287376220
#### 2026-01-30: https://x.com/trailblaziger/status/2017472750059672031
#### 2026-01-31: https://x.com/trailblaziger/status/2017840119986737579
#### 2026-02-01: https://x.com/trailblaziger/status/2018203182040601006
#### 2026-02-02: https://x.com/trailblaziger/status/2018562812553957427
#### 2026-02-03: https://x.com/trailblaziger/status/2018923759701225829
#### 2026-02-04: https://x.com/trailblaziger/status/2019288537712267630
#### 2026-02-05: https://x.com/trailblaziger/status/2019650332142497944
#### 2026-02-06: https://x.com/trailblaziger/status/2020010138174644501
#### 2026-02-07: https://x.com/trailblaziger/status/2020377398106018017
#### 2026-02-09: https://x.com/trailblaziger/status/2021097388354797949
#### 2026-02-10: https://x.com/trailblaziger/status/2021459604584997295
#### 2026-02-11: https://x.com/trailblaziger/status/2021824230518636566
#### 2026-02-13: https://x.com/trailblaziger/status/2022545000190312448
#### 2026-02-14: https://x.com/trailblaziger/status/2022907408641589651
#### 2026-02-15: https://x.com/trailblaziger/status/2023274252213043217
#### 2026-02-16: https://x.com/trailblaziger/status/2023638308962677117
#### 2026-02-17: https://x.com/trailblaziger/status/2024003602444861649
#### 2026-02-19: https://x.com/trailblaziger/status/2024718679334965267
#### 2026-02-21: https://x.com/trailblaziger/status/2025440569825395065
#### 2026-02-22: https://x.com/trailblaziger/status/2025808145709469833
#### 2026-02-23: https://x.com/trailblaziger/status/2026184230682624111
#### 2026-02-24: https://x.com/trailblaziger/status/2026537526870016172
#### 2026-02-27: https://x.com/trailblaziger/status/2027612029775749465
#### 2026-02-28: https://x.com/trailblaziger/status/2027980443614851303
