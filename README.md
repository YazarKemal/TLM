# ⚛️ TLM Scientific Laboratory v2.1

> **Temporal Localization Model (TLM) — Kuantum zaman-evrimi ve tersinirlik simülasyon arayüzü**
> **Geliştirici:** Kemal Çetin · ORCID: 0000‑0003‑7675‑0174
> **Canlı Demo:** [https://yazarkemal.github.io/TLM](https://yazarkemal.github.io/TLM)

---

## İçindekiler

1. [Proje Özeti](#proje-özeti)
2. [Öne Çıkan Özellikler](#öne-çıkan-özellikler)
3. [Hızlı Başlangıç](#hızlı-başlangıç)
4. [Dizin Yapısı](#dizin-yapısı)
5. [Bilimsel Arka Plan](#bilimsel-arka-plan)
6. [Katkıda Bulunma](#katkıda-bulunma)
7. [Lisans](#lisans)

---

## Proje Özeti

TLM Scientific Laboratory, **WASM + JS** tabanlı etkileşimli bir arayüzde kuantum master denklemlerini çözerek zaman akışını simüle eder ve *TLM Tersinirlik Protokolü* (η-parametrik Loschmidt geri dönüşü) ile entropik geri sarma deneyleri sunar.
Simülasyon kodu tamamen tarayıcıda çalıştığından ek sunucu altyapısı gerektirmez.

## Öne Çıkan Özellikler

| Modül                      | Açıklama                                                        |
| -------------------------- | --------------------------------------------------------------- |
| **Hamiltonyen Yapıcı**     | Serbest metin girdisi → n‑kubit Pauli operatör tensörlemesi     |
| **Monte Carlo Unraveling** | Çoklu koşuda istatistik toplayıp histogram grafiği üretir       |
| **Bloch Küresi**           | THREE.js tabanlı 3D görselleştirme, canlı döndürme              |
| **Matter.js Zaman Kutusu** | Klasik objelerin ileri/geri akışını görsel metafor olarak sunar |
| **Gerçek‑Zaman Metriği**   | Fidelity, Purity, von Neumann Entropisi ve Loschmidt Echo       |

## Hızlı Başlangıç

```bash
# 1 — Depoyu klonla
$ git clone https://github.com/YazarKemal/TLM.git && cd TLM

# 2 — Yerel sunucu başlat (Python örneği)
$ python -m http.server 8000

# 3 — Tarayıcıda aç
http://localhost:8000/index.html
```

> **Not:** `file:///` protokolü yerine yerel sunucu kullanmak CORS engellerini önler.

## Dizin Yapısı

```
TLM/
 ├─ index.html       # Tek sayfalık uygulama (SPA)
 ├─ assets/          # Logolar, ikonlar, ekran görüntüleri
 └─ README.md        # Proje dokümantasyonu (bu dosya)
```

## Bilimsel Arka Plan

* **Master Denklem:** Lindblad formu + fenomenolojik dekoherans
* **Loschmidt Echo:** |⟨ψ(0)|ψ(t)⟩|²; TLM’de η katsayısı ile geri sarma hassasiyeti
* **Entropy Ölçümü:** ρ² izi üzerinden Purity → von Neumann S = −Tr\[ρ log₂ρ]
* **Platform Parametreleri:** İyon tuzağı, SC qubit, fotonik ve NMR için T₁/T₂ & hata değerleri

> Ayrıntılı teorik açıklama için `docs/TLM_theory.pdf` (yakında) eklenecektir.

## Katkıda Bulunma

1. **Fork** → **Branch** → PR: `feature/<kısa-açıklama>`
2. Kod stiline uy: 2 boşluk, ES2021, `prettier` conf.
3. PR içinde *bilimsel gerekçeni* (deney/analiz) açıklayan kısa bir paragraf ekle.

## Lisans

Bu proje **MIT Lisansı** ile lisanslanmıştır — ayrıntılar için `LICENSE` dosyasına bakınız.
