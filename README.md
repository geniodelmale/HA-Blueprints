# HA-Blueprints

Lorenzo's Blueprints for Home Assistant:


[**♨️ Climate Set Last HVAC Action**](https://github.com/geniodelmale/HA-Blueprints/blob/main/blueprints/climate_set_last_HVAC.yaml): For Climate devices created using SmartIR and other sensors, so Home Assistant can keep track of the old status when the device is turned on from the physical remote.

    - Input: Climate Entity

[**Messaggio con attesa tra duplicati**](https://github.com/geniodelmale/HA-Blueprints/blob/main/blueprints/deduplicated_message.yaml): Script richiamabile con un parametro `message`. Invia subito i messaggi nuovi e scarta quelli uguali all'ultimo inviato finche non sono trascorse le ore configurate (da 0 a 24, default 24).

    - Configurare l'azione di notifica (Telegram o altro) usando `{{ message }}` come testo.
    - Creare e selezionare un helper `input_text` e un helper `input_datetime` con data e ora per conservare lo stato tra le esecuzioni.
    - Richiamare lo script passando il messaggio: `action: script.nome_script` e `data: { message: "Testo da inviare" }`.

[**♨️ Heating Blueprint**](https://github.com/geniodelmale/HEATHER-Home-Heating-Control-for-Home-Assistant-): This is a complex Blueprint, derived from Andy Simmons work. It's on a separate Repo with all the instructions, due to its complexity.