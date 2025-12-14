# 📊 Interactive Data Visualization Dashboard

A powerful, real-time data visualization tool that generates mathematical functions and displays them through interactive charts, statistical analysis, and matrix operations. Built with vanilla JavaScript, Chart.js, and Math.js.

## ✨ Features

### Core Functionality
- **Multiple Mathematical Functions**
  - Sine Wave
  - Cosine Wave
  - Tangent
  - Polynomial (quadratic)
  - Exponential decay with oscillation

- **Real-time Visualizations**
  - Interactive line chart for function plots
  - Histogram bar chart for data distribution
  - Smooth animations and transitions
  - Responsive chart resizing

- **Statistical Analysis**
  - Mean calculation
  - Standard deviation
  - Maximum value
  - Minimum value
  - All computed using Math.js library

- **Matrix Operations** (NumPy-like)
  - Matrix creation from data
  - Matrix transposition
  - Determinant calculation
  - Matrix multiplication
  - Formatted matrix display

### User Controls
- **Data Size**: 10-1000 data points
- **Function Type**: 5 different mathematical functions
- **Amplitude**: 0.1-10 adjustable amplitude
- **One-Click Generation**: Instant data generation and visualization

## 🎨 Design Features

- **Modern Gradient UI**: Purple-pink gradient background
- **Glassmorphic Cards**: Semi-transparent cards with backdrop blur
- **Hover Effects**: Interactive card animations
- **Responsive Layout**: Mobile-friendly grid system
- **Loading States**: Spinner animation during processing
- **Error Handling**: User-friendly error messages

## 🚀 Getting Started

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Internet connection (for CDN libraries)

### Installation

1. **Download the HTML file**
2. **Open in browser**: Double-click or right-click → Open with → Browser
3. **Start exploring**: No installation or setup required!

### Quick Start Guide

1. **Choose Your Function**
   - Select from the dropdown (Sine, Cosine, Tangent, Polynomial, Exponential)

2. **Adjust Parameters**
   - Set data size (10-1000 points)
   - Adjust amplitude (0.1-10)

3. **Generate Data**
   - Click "Generate New Data" button
   - Watch the visualizations update in real-time

4. **Analyze Results**
   - View the function plot (line chart)
   - Check data distribution (histogram)
   - Review statistics (mean, std dev, min, max)
   - Examine matrix operations

## 📈 Chart Details

### Function Plot (Line Chart)
- Displays the selected mathematical function
- X-axis: Input values (0 to 4π)
- Y-axis: Function output values
- Smooth curve with gradient fill
- Interactive tooltips on hover

### Data Distribution (Bar Chart)
- Shows frequency distribution in 10 bins
- Helps visualize data spread
- Color-coded bars
- Bin ranges labeled on X-axis

## 🔢 Mathematical Functions

### 1. Sine Wave
```
y = amplitude × sin(x)
```
Classic sinusoidal oscillation

### 2. Cosine Wave
```
y = amplitude × cos(x)
```
Phase-shifted sine wave

### 3. Tangent
```
y = amplitude × tan(x)
```
Clamped between -10 and 10 to handle asymptotes

### 4. Polynomial
```
y = amplitude × (0.1x² - 0.5x + 1)
```
Quadratic function with curvature

### 5. Exponential
```
y = amplitude × e^(-x/4) × sin(x)
```
Damped oscillation

## 🧮 Matrix Operations

The dashboard performs NumPy-like matrix operations:

### Operations Performed
1. **Matrix Creation**: Reshape 1D data into 2D matrix (up to 4×4)
2. **Transpose**: Flip rows and columns
3. **Determinant**: Calculate matrix determinant
4. **Multiplication**: Compute Matrix × Transpose

### Display Format
```
Original 4×4 Matrix:
   1.23    2.45    3.67    4.89
   5.01    6.23    7.45    8.67
   ...

Transpose:
   [Transposed values]

Determinant: [calculated value]

Matrix × Transpose:
   [Product matrix]
```

## 🛠️ Technical Stack

### Libraries
- **Chart.js 3.9.1**: Modern charting library
  - Beautiful, responsive charts
  - Smooth animations
  - Interactive tooltips

- **Math.js 11.11.0**: Mathematics library
  - Statistical functions
  - Matrix operations
  - NumPy-like API

### Technologies
- **HTML5**: Semantic structure
- **CSS3**: Modern styling with gradients, animations
- **Vanilla JavaScript**: No framework overhead

## 📱 Responsive Design

### Desktop (>768px)
- Two-column grid layout
- Full-width statistics row
- Optimal chart sizes

### Mobile (<768px)
- Single-column layout
- Stacked visualizations
- Touch-friendly controls
- Full-width inputs

## 🔧 Customization

### Changing Colors

**Background Gradient:**
```css
body {
    background: linear-gradient(135deg, #YOUR_COLOR1 0%, #YOUR_COLOR2 100%);
}
```

**Chart Colors:**
```javascript
// Line chart
borderColor: 'rgb(79, 70, 229)',
backgroundColor: 'rgba(79, 70, 229, 0.1)',

// Bar chart
backgroundColor: 'rgba(16, 185, 129, 0.8)',
```

### Adding New Functions

Add to the function selector:
```html
<option value="your_function">Your Function</option>
```

Add to the switch statement:
```javascript
case 'your_function':
    y = amplitude * yourFormula(x);
    break;
```

### Adjusting Chart Options

Modify chart configuration:
```javascript
options: {
    responsive: true,
    scales: {
        y: { beginAtZero: true },
        // Add your customizations
    }
}
```

## 🐛 Fixed Issues

### Improvements from Original
1. ✅ **Enhanced Error Handling**: Try-catch blocks throughout
2. ✅ **Input Validation**: Checks for valid data ranges
3. ✅ **NaN/Infinity Filtering**: Removes invalid data points
4. ✅ **Better Chart Performance**: Disabled animation on updates
5. ✅ **Improved Tangent Function**: Proper value clamping
6. ✅ **Error Messages**: User-friendly error display
7. ✅ **Button State Management**: Proper disable/enable on generate
8. ✅ **Mobile Responsiveness**: Better control layouts
9. ✅ **Chart Tooltips**: Enhanced interactivity
10. ✅ **Matrix Error Handling**: Graceful failure for singular matrices

## 🎯 Use Cases

### Educational
- Teaching mathematical concepts
- Demonstrating statistical analysis
- Visualizing function behavior
- Learning matrix operations

### Professional
- Data analysis prototyping
- Algorithm visualization
- Mathematical modeling
- Performance demonstrations

### Personal
- Exploring mathematical patterns
- Portfolio project
- Learning Chart.js and Math.js
- Frontend development practice

## 🚀 Future Enhancements

### Potential Features
- **Export Options**: Save charts as images (PNG/SVG)
- **Data Import**: Load custom datasets from CSV/JSON
- **More Functions**: Add logarithmic, hyperbolic, custom functions
- **3D Visualizations**: Surface plots using Three.js
- **Animation Controls**: Play/pause function animation
- **Comparison Mode**: Display multiple functions simultaneously
- **Color Themes**: Light/dark mode toggle
- **Advanced Matrix Ops**: Eigenvalues, eigenvectors, SVD
- **Statistical Tests**: Correlation, regression analysis
- **Data Persistence**: Save/load configurations

### Integration Ideas
- Connect to real-time data APIs
- Backend for user accounts
- Collaborative features
- Export to Python/MATLAB code
- Integration with Jupyter notebooks

## 📊 Performance

### Optimization Tips
- Use smaller data sizes (50-200) for smooth animation
- Larger sizes (500-1000) for detailed analysis
- Chart updates use 'none' animation mode for speed
- Efficient data filtering removes invalid values

### Browser Performance
- **Chrome/Edge**: Excellent (recommended)
- **Firefox**: Excellent
- **Safari**: Very good
- **Mobile**: Good (use smaller data sizes)

## 🔐 Security

- No external data transmission
- All computations client-side
- No user data stored
- Safe CDN library loading
- No authentication required

## 📄 License

Open source and free to use for personal and commercial projects.

## 🤝 Contributing

Contributions welcome! Areas for improvement:
- Additional mathematical functions
- New visualization types
- Performance optimizations
- Accessibility enhancements
- Documentation improvements

## 💡 Tips & Tricks

1. **Best Data Size**: 50-100 points for balanced performance and detail
2. **Tangent Function**: Creates interesting patterns but watch for discontinuities
3. **Amplitude Effects**: Try extreme values (0.1, 10) for dramatic differences
4. **Matrix Operations**: Work best with data size ≥ 16 (for 4×4 matrix)
5. **Mobile Usage**: Use smaller data sizes for better performance

## 🙏 Acknowledgments

- Chart.js team for excellent charting library
- Math.js team for powerful mathematical toolkit
- Inspired by NumPy, MATLAB, and scientific computing tools

---

**Built with ❤️ for data enthusiasts and mathematicians**

*Version 2.0 (Fixed & Enhanced) - December 2025*
