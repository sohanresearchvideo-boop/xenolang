xenolang
├── data/
│   ├── ingestion/        # readers for each sensor format
│   ├── corpus/           # downloaders for Macaulay, Watkins, ESP, Xeno-canto
│   └── schema.py         # the unified data contract from A7
├── preprocessing/
│   ├── denoise.py
│   ├── source_separation.py
│   ├── fft_features.py   # the "Ryland chord-decomposer"
│   └── pose_extraction.py
├── models/
│   ├── primary_ai/       # Earth Species matcher
│   │   ├── encoder.py    # fine-tune AVES / NatureLM
│   │   └── matcher.py    # nearest-neighbor over embeddings
│   └── secondary_ai/     # Structural analysis module
│       ├── zipf.py
│       ├── entropy.py
│       ├── segmentation.py
│       └── cross_modal.py
├── synthesis/
│   ├── decoder.py        # VAE: embedding → waveform
│   └── playback_planner.py
├── api/
│   └── server.py         # FastAPI: tagging, inference, playback endpoints
├── ui/
│   └── (React app)
├── notebooks/            # exploration, validation
└── tests/
