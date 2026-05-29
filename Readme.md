# SSH Log Anomaly Detector 🔐

## What it does
It parses SSH authentication logs to detect brute-force attacks and suspicious login patterns.

## Sample output (screenshot)
| IP | Severity | Failed Attempts | Successful Login |
|---|---|---|---|
| 172.16.0.8 | HIGH | 10 | No |
| 192.168.1.10 | CRITICAL | 5 | YES |
| 203.0.113.45 | CRITICAL | 5 | YES |
| 10.0.0.99 | HIGH | 6 | No |

Peak attack hour: May 15 10:02 (10 attempts)

## Requirements
Python 3.x — no external libraries needed

## Usage
python analyzer.py --log auth.log --threshold 5
