# netflow-viz

![Python](https://img.shields.io/badge/Python-3.10+-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-In%20Progress-orange)

An interactive network traffic anomaly visualizer. Parse PCAP files or
Zeek/Suricata logs and explore your network through connection graphs,
time-series anomaly plots, and protocol breakdowns — all in a browser dashboard.

## Features
- Parse PCAP files (via Scapy/PyShark) and Zeek conn.log files
- Interactive connection graph (who talked to whom)
- Time-series traffic volume with anomaly markers (Z-score / IQR)
- Protocol distribution charts
- Top talkers and suspicious IP flagging
- REST API backend (Flask) + interactive frontend (Plotly.js / D3.js)

## Tech Stack
`Python` `Scapy` `PyShark` `Flask` `Plotly.js` `pandas` `scipy`

## Project Structure
```
netflow-viz/
├── parser/
│   ├── pcap_parser.py      # PCAP to DataFrame
│   └── zeek_parser.py      # Zeek conn.log parser
├── api/
│   └── app.py              # Flask REST endpoints
├── frontend/
│   ├── index.html
│   ├── graph.js            # Connection graph
│   └── charts.js           # Time-series + protocol charts
├── samples/                # Public PCAP samples for testing
├── tests/
├── requirements.txt
└── README.md
```

## Getting Started
```bash
git clone https://github.com/SANC18/netflow-viz
cd netflow-viz
pip install -r requirements.txt
python api/app.py
# Open http://localhost:5000
# Upload a PCAP file and explore
```

## Roadmap
- [x] Project structure setup
- [ ] PCAP parser (Scapy)
- [ ] Zeek log parser
- [ ] Flask API endpoints
- [ ] Connection graph (D3.js)
- [ ] Anomaly detection (Z-score)
- [ ] Frontend dashboard
- [ ] Deploy to Render

## License
MIT
