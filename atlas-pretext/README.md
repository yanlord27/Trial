# Atlas — PreTeXt migration

This is a modular PreTeXt source project converted from Atlas v9. It is not a compiled website. The PreTeXt CLI could not be installed in the conversion environment (network unavailable), so schema validation and official HTML build remain to be done.

On macOS, with Python installed, open Terminal in this directory:

```sh
python3 -m venv .venv
source .venv/bin/activate
python -m pip install pretext
pretext build html
pretext view html
```

The main source is `source/main.ptx`; each course has its own chapter file. Existing outline sections remain marked as planned. The original reference index is preserved separately. Explicit math delimiters from v9 were converted to `m` and `me` elements; legacy fragmented notation still requires editorial review. Unambiguously associated proofs use native proof elements; other proof notes are preserved as titled remarks to avoid attaching them to the wrong theorem. Review tracking and the cyclic group interactive widget are not yet ported; the original v9 remains the working fallback.
