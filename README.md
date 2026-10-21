# extract

Utility that turns raw Persian text cells copied from university admission tables (PDF sources) into a clean three-column dataset: **university, province, study location**.

`extractUNI.py` contains the raw cell strings, annotated with their source page. `clean_and_parse()` strips codes and boilerplate, standardises separators and uses regular expressions plus a province lookup to recognise Payam Noor units and general university/location patterns. The de-duplicated, sorted result is printed and saved as `extracted_universities.csv` (UTF-8 with BOM, ready for Excel).

## Requirements

Python 3.9+; standard library only (`csv`, `io`, `re`).

```bash
python extractUNI.py
```
