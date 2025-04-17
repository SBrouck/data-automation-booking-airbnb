# data-automation-booking-airbnb
Automated pipeline for consolidating Airbnb and Booking.com reservation data into a unified Excel report. Combines past revenue exports with future iCal-based calendars, enabling streamlined reporting and analytics for short-term rental businesses.
# Rental Data Pipeline

This project automates the collection, cleaning, and consolidation of short-term rental data from Airbnb and Booking.com into a unified Excel report.  
It combines historical reservation exports with up-to-date future bookings extracted from public iCal calendar links, enabling structured reporting and deeper performance analysis.

## 🌍 Real-world context

This workflow was initially developed as part of my personal work while managing data for an international real estate portfolio worth €50M.  
It allowed me to significantly reduce manual data handling and streamline weekly reporting across multiple rental platforms.

---

## 📦 What it does

- Parses and cleans Airbnb exports (Excel format)
- Parses and cleans Booking.com exports (CSV format)
- Pulls real-time future reservations from Airbnb iCal calendar URLs
- Merges all data into one Excel file with two sheets:
  - `Revenus_passés`: all past reservations from both platforms, sorry for the french words :)
  - `Calendrier_a_venir`: upcoming bookings pulled from iCal

---

## 🚀 How to use it (via Google Colab)

1. Open the notebook in **Google Colab** (no installation required)
2. Upload:
   - A `.csv` export from Booking.com
   - A `.xlsx` export from Airbnb
3. (Optional) Customize the `ICAL_LINKS` section with your own Airbnb calendar URLs
4. Run all cells
5. Download the generated Excel file `reservation_summary.xlsx`

---

## 📸 Output preview

Here’s an example of the final Excel file with structured past and future reservation data:

![Reservation summary preview](assets/reservation-summary-output.png)


## 🧰 Required input format

### Booking.com (CSV)
The file must include at least the following columns:
- `Listing`, `Guest name`, `Start date`, `End date`, `# of nights`, `Earnings`

### Airbnb (Excel)
The file must include at least the following columns:
- `Nom de l'établissement`, `Nom du client`, `Arrivée`, `Départ`, `Paiement total`

You can adapt the column names in the script if your exports differ.

---

## 🧠 Why this matters

Short-term rental operators often manage data across multiple platforms and formats. This tool enables:

- Centralized data access across Airbnb and Booking.com
- Faster reporting workflows
- Integration-ready Excel format for financial or occupancy analysis
- Full reproducibility in a cloud environment

---

## 📈 Ideas for future enhancements

- Dashboard generation (monthly revenue, occupancy rate)
- Google Sheets integration
- Email automation for weekly reports
- Support for channel manager APIs

---

## 📄 License

This project is open-source and free to use for personal or professional purposes. Attribution is appreciated if you adapt it.

