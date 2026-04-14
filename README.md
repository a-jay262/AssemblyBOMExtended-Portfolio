# AssemblyBOMExtended

**Dynamics 365 Business Central Extension**  
*Real-time Unit Cost & Unit Price visibility with UOM-aware calculations for Assembly BOMs*

---

## 📋 Project Overview

This extension enhances the standard **Assembly BOM** functionality in Business Central by automatically displaying and calculating:

- Unit Cost and Unit Price per BOM component
- Total Line Cost and Total Line Price
- Aggregated BOM Totals (Cost & Price)
- Estimated BOM Cost & Price directly on the **Item Card**

It intelligently handles **Unit of Measure** conversions, ensuring accurate costing even when BOM lines use different UOMs than the item's base unit.

---

## ✨ Key Features

- Real-time recalculation on changes to `No.`, `Quantity per`, and `Unit of Measure Code`
- Proper **UOM Conversion** logic (Base UOM → BOM UOM)
- Live **BOM Totals** section at the bottom of the Assembly BOM page
- Smart visibility of BOM estimates on Item Card (only for Assembly items)
- FlowField-based rollups for best performance
- Clean, non-intrusive UI integration

---

## 🛠 Technical Highlights

- **Table Extensions** on `BOM Component` and `Item`
- **Page Extensions** on Assembly BOM and Item Card
- Centralized calculation logic in `CalculateLineAmounts()` procedure
- Event-driven updates using `OnAfterValidate` and `OnAfterGetRecord`
- Smart visibility pattern to avoid unnecessary page refreshes

### Version History

- **27.0.0.0** — Initial release
- **27.0.0.1** — Added fields on Item Card + BOM Totals
- **27.0.0.2** — Implemented UOM handling
- **27.0.0.3** — Fixed UOM conversion for Unit Price & Cost

---

## 📸 Screenshots

**Assembly BOM Page with Cost & Price Columns**  
![Assembly BOM Enhanced](images/assembly-bom.png)

**Item Card - Estimated BOM Totals**  
![Item Card](images/item-card.png)

*(Add your screenshots in the `images/` folder)*

---

## 🚀 Installation

1. Download or clone this repository
2. Open the project in Visual Studio Code with AL Language extension
3. Update `app.json` with your publisher details and ID range
4. Publish the extension to your Business Central environment
5. Test on any Item with Assembly BOM enabled

---

## 💡 Best Practices Applied

- Logic centralized in Table Extension (reusable & maintainable)
- Efficient use of FlowFields for totals
- Proper handling of different Units of Measure
- Clean trigger usage for real-time experience

---

## 📄 License

This is a **personal portfolio project** showcasing my Dynamics 365 Business Central development skills.  
Source code is provided for demonstration purposes only.

---

**Alishba**  
Dynamics 365 Business Central Developer  
Lahore, Pakistan

---

**This project demonstrates my ability to deliver practical, user-focused enhancements with proper AL coding standards and business logic.**
