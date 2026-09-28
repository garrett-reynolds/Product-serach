```
Subject:      Vending tray / slot that runs either a spiral coil or a belt conveyor
Prepared:     Sep 28 2026
Skill:        parts-sourcing
Currency:     CAD $ · USD 1.4145, EUR 1.6122 (Bank of Canada daily avg, Sep 25 2026)
Tax:          HST 13% excluded
Verification: [V] = read from the vendor's own source on the prepared date · [T] = third-party only · [U] = unverified
```

## Bottom line

KioSoft (now trading as PayRange) doesn't swap a coil for a belt inside a slot. Its machines take **separate spiral trays and belt trays**, each of which unplugs from the machine through one cable connector at the back. That makes the Mississauga office the fastest way to get a matched pair. For a lane-level swap that shares one motor and one drive board, the part to buy is a Chinese 24 VDC "spring-machine compatible" belt lane (Huansheng or Yemchang). Neither publishes a price, so both need an RFQ.

## How the swap actually works

| Architecture | What changes on swap | What stays | Source |
|---|---|---|---|
| KioSoft / PayRange trays [V] | Whole tray (spiral tray ↔ belt tray) | Slide rails, tray cable connector, controller | support.kiosoft.com Adjust Tray Height / Belt Slots / Spiral Slots |
| Generic Chinese spring-machine lane [V] | Spiral + clutch → belt lane + coupling | 24 VDC slot motor, drive board, wiring | Huansheng listing; Vendy1 tray-swap settings |
| Drive-board config after swap [V] | Each slot must be set to "Spring" or "Belt" in firmware | — | vendy1.com tray-exchange settings ("Work in Belts") |

## Options

| # | Part | Supplier | Key spec | Price (CAD) | Stock / lead | Risk | Ver. |
|---|---|---|---|---|---|---|---|
| 1 | Spare spiral tray + belt tray for KioVend TSD-series | KioSoft/PayRange Canada, 5610 Kennedy Rd, Mississauga ON · (855) 856-6398 | Tray-level swap, same connector. Belt slots need products < 100 mm long | Not published | Not published. Machines are built in their Florida or Toronto warehouse [T] | Trays may only be sold with machines. Only fits their machines | [V] contact, docs · [T] warehouse |
| 2 | Vending machine conveyor belt lane, 140 × 58 × 43 mm | Huansheng (Shijiazhuang, CN) · hauncheon@outlook.com · +86 311 6769 9817 | 24 VDC integrated gear motor. "Compatible with spring machine drive boards" | Not published | Not published | Import. Short lane, sized for small boxed goods | [V] |
| 3 | Vending machine conveyor tray, "interchangeable with springs" | Yemchang (CN) | 12 or 24 VDC gear motor. Keeps original lane, electrics and terminal socket. 10 kg single / 20 kg double tray | Not published | Not published | Site returned 503. Specs come from search snippets only | [T] |
| 4 | LY-M8 24 VDC single spring motor (drives spiral or belt coupling) | Guangdong Lingye, via made-in-china.com | 24 VDC. RPM and feedback switch not published | CAD $7.07/unit (US$5) at 100–200 pcs, before shipping, duty and brokerage | MOQ 100 | MOQ price only. No spec sheet | [V] price |
| 5 | Coupling for conveyor belt (TCN-style) | Vendy1 (Germany) | Links the slot motor to the belt roller | CAD $8.06 (€5.00), before shipping | Not published | EU import. Only fits TCN-pattern lanes | [V] |
| 6 | 460 × 85 mm stainless mini conveyor lane, 24 VDC, 3.5–5 kg, ~35 RPM | Amazon.ca (ASIN B0C89J1KB1, B0DQL4B76N) | Standalone lane with its own motor. Listing says it suits spring-type machines | Not published (page wouldn't load) | Not published | Marketplace seller, batch varies. Not a drop-in for a spiral slot | [T] |
| 7 | Robomarket R1-i88 Max / R2-i88 Slim / Outdoor series | Eflyn Canada, 2660 Meadowvale Blvd Unit 6A, Mississauga ON · 657-413-8337 | "Horizontal pushing slots" on 6 shelves, 84 selections, 539–819 pcs, X-Y robot arm + elevator pickup, BLDC motor rated 250,000 cycles, MDB/DEX/RS232 | Not published | Not published | **Not coil or belt.** Pusher lanes only, so no coil/belt swap. Whole machine, 516 kg | [V] |
| 8 | Local parts and service | Kane's Distributing (Ontario) · 905-688-8823 | Vending equipment sales and service | Not published | Phone | Mostly refurbished branded machines | [T] |

## Red flags

- **Motor voltage.** Lanes come in 12 VDC and 24 VDC versions. Match your drive board before ordering. No-load current is under 180 mA at 24 V and under 280 mA at 12 V [T].
- **Stop logic differs.** A spiral stops on the motor's one-revolution cam switch. A belt usually relies on a timer or a drop sensor. The controller has to be told which is which (see the Vendy1 settings above), and a belt left in spring mode will under- or over-dispense.
- **Product geometry.** On KioSoft belt slots, products must be under 100 mm long, not too light (light items spin and false-trigger the sensor), and must stand on their own without leaning [V].
- **No standard lane pitch or connector.** TCN, KioSoft and generic Chinese lanes aren't cross-compatible. Buy trays and lanes from the same platform as your machine or controller.
- **MOQ.** The Lingye price only applies from 100 pieces.

## Sources & verification

- kiosoft.com/vending-machines: models, dispense types, Canada office [V]
- support.kiosoft.com/docs/spiral-slots.md, belt-slots.md, 1refund-creditcard-12.md (Adjust Tray Height) [V]
- hauncheon.com/vending-machine-conveyor-belt-product/ [V]
- lingyevending.en.made-in-china.com/product/xfkYmjrJBDWQ/ [V]
- vendy1.com/accessories/spare-parts/ and vendy1.com/help-center/5-inch-machine/trays-exchanged-settings/ [V]
- yemchang.com/vending-parts/vending-machine-conveyor-tray.html: 503, search snippet only [T]
- amazon.ca/dp/B0C89J1KB1, amazon.ca/dp/B0DQL4B76N: bot-blocked, title and snippet only [T]
- shop.quickfreshvending.com/product/spiral-belt-slot-motor/: bot-blocked, not used
- eflyn.com/catalog/robomarket-smart-micro-market-vending-machine-max-series/, -slim-series/, robomarket-smart-vending-machine-outdoor-series-with-optional-smart-locker/ [V]
- vendingconnection.com Canadian suppliers list (Kane's) [T]
- bankofcanada.ca Valet API FX [V]
- Not checked: landed cost for any import (no prices published), and whether KioSoft sells trays separately.

## NEEDS YOU

1. Call KioSoft/PayRange Canada at (855) 856-6398 and ask whether spiral and belt trays for the TSD48 are sold as spares, at what price, and what the motor voltage is.
2. Tell me the quantity and whether you're modifying an existing machine or building a custom one. That decides between KioSoft trays and a Chinese lane RFQ.
3. If you're building custom, send an RFQ to hauncheon@outlook.com for belt lanes plus matching spirals on the same 24 VDC motor, asking for price, MOQ, lead time and the stop-switch type.
