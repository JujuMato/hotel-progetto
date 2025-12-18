---
title: "APPLICAZIONE WEB CON DATABASE"
author: "Lucianaz Julien - Classe 5C IT"
date: "{{date}}"
---

# APPLICAZIONE WEB CON DATABASE

## Indice
- [Introduzione](#introduzione)
- [Analisi dei requisiti](#analisi-dei-requisiti)
- [Diagramma Entità-Relazione](#diagramma-entità-relazione)
- [Schema logico](#schema-logico)
- [Dizionario dei dati](#dizionario-dei-dati)
- [Conclusioni](#conclusioni)

---

## Introduzione

Il presente progetto riguarda la progettazione di un database relazionale per un sistema di gestione di un hotel, da utilizzare come base per un’applicazione web.  
Il sistema è pensato per supportare tutte le principali attività operative di una struttura alberghiera, consentendo una gestione efficiente e integrata di clienti, prenotazioni, camere, servizi, personale, fatturazione e manutenzioni.

La progettazione del database rappresenta la Fase 1 dello sviluppo dell’applicazione e ha l’obiettivo di realizzare una struttura dati affidabile, coerente e facilmente estendibile, rispettando i vincoli reali di un contesto alberghiero, come la gestione delle prenotazioni nel tempo e il controllo dell’occupazione delle camere.

---

## Analisi dei requisiti

### Requisiti funzionali

Il sistema deve consentire di:
- gestire i clienti memorizzandone i dati anagrafici e di contatto;
- gestire le prenotazioni indicando il periodo di soggiorno e lo stato;
- gestire le camere con informazioni su numero, piano, prezzo e disponibilità;
- classificare le camere tramite i tipi di camera;
- gestire il soggiorno effettivo del cliente;
- registrare i servizi offerti dall’hotel;
- tracciare i consumi effettuati durante il soggiorno;
- gestire la fatturazione e i pagamenti;
- gestire il personale e i relativi turni di lavoro;
- gestire la manutenzione delle camere.

### Vincoli di sistema

- Una camera può avere più prenotazioni, ma in periodi diversi;
- Ogni prenotazione è associata a una sola camera;
- Una fattura può essere saldata tramite uno o più pagamenti;
- I dati devono rispettare i vincoli di integrità referenziale;
- Il database deve evitare ridondanze e anomalie di aggiornamento.

---

## Diagramma Entità-Relazione

Il diagramma Entità-Relazione descrive la struttura concettuale del database, evidenziando le entità principali, i loro attributi e le relazioni con le rispettive cardinalità.

Le entità individuate sono:
- Cliente
- Prenotazione
- Camera
- TipoCamera
- Soggiorno
- Servizi
- Consumi
- Fattura
- Pagamenti
- Personale
- Turni
- Manutenzione

Le relazioni modellano il funzionamento reale dell’hotel:
- Un cliente può effettuare più prenotazioni;
- Una prenotazione genera un soggiorno;
- Una camera appartiene a un solo tipo di camera;
- Durante il soggiorno vengono registrati i consumi dei servizi;
- Una prenotazione genera una fattura;
- Una fattura può essere pagata con più pagamenti;
- Il personale svolge turni di lavoro e interventi di manutenzione.

Il diagramma ER è rappresentato tramite codice Mermaid.

