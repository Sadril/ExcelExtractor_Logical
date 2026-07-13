# Excel Comment Processor

[![Python Version](https://img.shields.io/badge/python-3.14%2B-blue.svg)](https://python.org)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows-blue.svg)](https://microsoft.com/windows)
[![Version](https://img.shields.io/badge/version-1.0.0-orange.svg)](https://github.com/yourusername/excel-comment-processor)

A powerful desktop application to extract names and LOGICAL entries from Excel and CSV comments. Perfect for network operations teams and system administrators who need to analyze communication logs and comments.

## 🎯 Overview

**Excel Comment Processor** is a standalone Windows application that automatically extracts:
- **Names** from comments containing `[name][NOC]` patterns
- **LOGICAL entries** like `LOGICAL_MISCONFIG`, `LOGICAL_Core_MISMATCH`, etc.
- **Associates** each name with its corresponding LOGICAL entries

This tool is particularly useful for NOC (Network Operations Center) teams who need to analyze communication logs and extract meaningful information from technical comments.

## ✨ Features

### Core Features
- ✅ **Dual Input Support** - Accepts both Excel (.xlsx, .xls) and CSV (.csv) files
- ✅ **Intelligent Extraction** - Extracts names with associated LOGICAL entries only
- ✅ **Professional Output** - Generates formatted Excel (.xlsx) files with colored headers
- ✅ **User-Friendly Interface** - Clean GUI with progress tracking
- ✅ **Flexible Output** - Choose any location to save results
- ✅ **Case Insensitive** - Handles LOGICAL entries regardless of case (e.g., LOGICAL_Core_MISMATCH)

### Technical Features
- ✅ **Multi-threaded Processing** - GUI remains responsive during processing
- ✅ **Real-time Progress** - Progress bar shows processing status
- ✅ **Detailed Logging** - Timestamped logs with color-coded messages
- ✅ **Auto-column Detection** - Automatically finds required columns
- ✅ **Standalone Executable** - No Python installation required for end users
- ✅ **Portable** - Run from USB drive or any folder

### Sample Input Data
| ticket_id | scomm_comments |
|-----------|----------------|
| TKT-001 | [oss_bot][10][2026-02-11 01:20:41]: NGSDR110HTR01_NGFAT3 to NGSDR076HTR01_NGHRP1 is down[shusmoy.kundu][NOC][2026-02-11 22:38:08]: [LOGICAL_MISCONFIG]\n[LOGICAL_SCRIPT_CONVERSION]\n[LOGICAL_ROUTER_PORT_CHANGE] |
| TKT-002 | [hannan.hossain][NOC][2026-02-18 18:56:18]: [LOGICAL_JOINT_CHECK] |

### Sample Output Data
| ticket_id | scomm_comments | extracted_name | logical_work_type |
|-----------|----------------|----------------|-------------------|
| TKT-001 | [oss_bot]... | shusmoy.kundu | LOGICAL_MISCONFIG, LOGICAL_SCRIPT_CONVERSION, LOGICAL_ROUTER_PORT_CHANGE |
| TKT-002 | [hannan.hossain]... | hannan.hossain | LOGICAL_JOINT_CHECK |

## 🚀 Installation

### For End Users (Recommended)
1. Download the latest `Excel Comment Processor.exe` from the [Releases](https://github.com/yourusername/excel-comment-processor/releases) page
2. Double-click to run - **No installation required!**
3. The tool works immediately on any Windows computer

