# Dashboard-Standalone

Dieses Verzeichnis ist der Startpunkt fuer die Auslagerung des Python-Dashboards in ein eigenstaendiges Projekt/Repository.

## Aktueller Zweck

- Spiegel des bisherigen Dashboards aus `Modules/Monitor/PythonDashboard`
- Kann als eigenes Repo versioniert werden
- GUI kann den Pfad ueber `config.json -> DashboardSettings.ProjectPath` auf dieses Verzeichnis zeigen

## Start (manuell)

```powershell
Set-Location .\Dashboard-Standalone
python -m pip install -r requirements.txt
python -m uvicorn app:app --host 127.0.0.1 --port 9500
```

## Wichtiger Hinweis

`Start-PythonDashboardBackground.ps1` unterstuetzt jetzt variable Projektpfade und nutzt fuer gemeinsame Logs optional die Umgebungsvariable `BOCKIS_GUI_ROOT`.
