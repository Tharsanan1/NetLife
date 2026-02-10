# NetLife - Time Management Visualization 📊

> **Visualize and take control of your time**

NetLife is a beautiful, interactive single-page application that helps you understand how you spend your time. Using an animated pie chart, you can see at a glance where your hours go and how much of your life remains in your control.

![NetLife Desktop View](https://github.com/user-attachments/assets/a233b534-c1da-4d68-8dea-ffad75218aea)

## ✨ Features

- 🎨 **Animated Pie Chart** - Beautiful, smooth animations show your time allocation
- 📅 **Multiple Frequencies** - Track time spent daily, on weekdays, weekends, weekly, monthly, or yearly
- 🧮 **Smart Calculations** - Automatically converts all entries to yearly hours for accurate percentages
- 💾 **Persistent Storage** - Your entries are saved locally and persist across sessions
- 📱 **Fully Responsive** - Works perfectly on mobile, tablet, and desktop devices
- 🎯 **Control Indicator** - See at a glance what percentage of your life you have in your control
- 🌈 **Color-Coded Entries** - Each activity gets its own distinctive color
- ⚡ **Lightning Fast** - Built with Astro for optimal performance

## 🚀 Live Demo

Visit the live application: [https://Tharsanan1.github.io/NetLife](https://Tharsanan1.github.io/NetLife)

## 📱 Screenshots

### Desktop Experience

**Initial State - 100% Free Time**
![Desktop Initial](https://github.com/user-attachments/assets/7229ef8c-6bf3-4367-aba7-e29f58922ac1)

**Adding a New Entry**
![Desktop Form](https://github.com/user-attachments/assets/1c841b64-3bcc-4699-a7d9-73364c597f19)

**Multiple Time Entries**
![Desktop Multiple](https://github.com/user-attachments/assets/a233b534-c1da-4d68-8dea-ffad75218aea)

### Mobile & Tablet

**Mobile View (iPhone)**
![Mobile](https://github.com/user-attachments/assets/5bc90881-960b-45f0-9bda-4577ef05f677)

**Tablet View (iPad)**
![Tablet](https://github.com/user-attachments/assets/3cd8d6fb-14d2-44e7-a22c-e9e89277c6ff)

## 🎯 How to Use

1. **Click the `+` Button** - Start by adding your first time entry
2. **Select Frequency** - Choose how often you do this activity:
   - **Daily** - Something you do every day (e.g., sleep, meals)
   - **Weekdays** - Monday through Friday activities (e.g., work)
   - **Weekends** - Saturday and Sunday activities (e.g., hobbies)
   - **Weekly** - Once per week activities (e.g., class, meeting)
   - **Monthly** - Once per month activities (e.g., hometown visit)
   - **Yearly** - Annual activities (e.g., vacation)
3. **Describe the Activity** - Give it a name (e.g., "Work", "Sleep", "Exercise")
4. **Enter Hours** - How many hours per occurrence (e.g., 8 hours of sleep daily)
5. **Save** - Watch the pie chart animate to show your new time allocation!
6. **View Your Control** - See the percentage of free time displayed at the top

### Example Entries

- **Sleep**: 8 hours, Daily → 2,920 hours/year (33.3%)
- **Work**: 8 hours, Weekdays → 2,080 hours/year (23.7%)
- **Self-care**: 3 hours, Daily → 1,095 hours/year (12.5%)
- **Hometown Visit**: 5 hours, Monthly → 60 hours/year (0.7%)

**Result**: You have ~30% of your life in your control!

## 🛠️ Tech Stack

- **[Astro](https://astro.build/)** - Modern static site generator
- **TypeScript** - Type-safe JavaScript
- **Canvas API** - For the animated pie chart
- **CSS3** - Responsive design with modern features
- **GitHub Actions** - Automated deployment

## 💻 Local Development

### Prerequisites

- Node.js 18+ 
- npm or yarn

### Setup

```bash
# Clone the repository
git clone https://github.com/Tharsanan1/NetLife.git
cd NetLife

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

The application will be available at `http://localhost:4321/NetLife`

## 📐 How It Works

### Time Calculation

NetLife calculates everything based on a standard year:
- **1 Year** = 365 days = 8,760 hours

Different frequencies are converted as follows:
- **Daily**: hours × 365
- **Weekdays**: hours × 260 (52 weeks × 5 days)
- **Weekends**: hours × 104 (52 weeks × 2 days)
- **Weekly**: hours × 52
- **Monthly**: hours × 12
- **Yearly**: hours × 1

### Free Time Calculation

```
Free Time % = (8,760 - Total Used Hours) / 8,760 × 100
```

## 🚀 Deployment

This project is configured for automatic deployment to GitHub Pages via GitHub Actions.

### Enable GitHub Pages

1. Go to your repository **Settings** → **Pages**
2. Under **Source**, select **GitHub Actions**
3. Push to the `main` branch
4. Your site will be live at `https://[username].github.io/NetLife`

### Manual Deployment

```bash
npm run build
# Upload the contents of the `dist` folder to your hosting provider
```

## 🎨 Customization

### Change Colors

Edit the color palette in `src/pages/index.astro`:

```typescript
const colors = [
  '#FF6384', // Pink
  '#36A2EB', // Blue
  '#FFCE56', // Yellow
  '#4BC0C0', // Teal
  '#9966FF', // Purple
  // Add more colors...
];
```

### Modify Time Calculations

Adjust the frequency calculations in the `calculateYearlyHours` function in `src/pages/index.astro`.

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 💡 Inspiration

This project was inspired by the idea that understanding how we spend our time is the first step to taking control of our lives. By visualizing our commitments, we can make more informed decisions about where to invest our most precious resource: time.

## 🐛 Known Issues

- Year calculations use 365 days (non-leap year) for consistency
- Weekdays calculation assumes exactly 260 days per year

## 🔮 Future Enhancements

- [ ] Export/Import data functionality
- [ ] Dark mode support
- [ ] Custom color picker for entries
- [ ] Comparison mode (week vs week, month vs month)
- [ ] Time optimization suggestions
- [ ] Share your time breakdown as an image
- [ ] Multiple pie chart views (daily, weekly, monthly)

## 📧 Contact

For questions, suggestions, or feedback, please open an issue on GitHub.

---

**Made with ❤️ using Astro**