# Network Routing Simulator - OSPF Protocol

A comprehensive web-based simulator for demonstrating **Shortest Path Tree (SPT) Optimization in Link State Routing** using the OSPF (Open Shortest Path First) protocol. This interactive tool allows users to visualize network topologies, calculate optimal routing paths, and simulate router failures to understand how link-state routing protocols adapt to network changes.

## 🚀 Features

### Core Functionality
- **Interactive Network Setup**: Create custom network topologies with configurable routers and links
- **Link State Packet (LSP) Generation**: Automatically generates LSPs for each router showing neighbor information
- **Shortest Path Calculation**: Implements Dijkstra's algorithm to find optimal routes
- **Routing Table Generation**: Displays complete routing tables for all routers
- **Router Failure Simulation**: Test network resilience by simulating router failures
- **Visual Network Graph**: Interactive network visualization using vis.js

### Advanced Features
- **Real-time Path Optimization**: Recalculates routes when network topology changes
- **Cost-based Routing**: Uses weighted edges to represent link costs
- **Failure Recovery**: Shows how the network adapts when routers fail
- **Multiple Router Support**: Supports networks with any number of routers
- **Responsive Design**: Works on desktop and mobile devices

## 🛠️ Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript (ES6+)
- **Visualization**: [vis.js Network](https://visjs.org/) for interactive network graphs
- **Algorithm**: Dijkstra's shortest path algorithm
- **Styling**: Custom CSS with modern gradient design
- **Architecture**: Client-side only (no backend required)

## 📁 Project Structure

```
SPT_Optimization_in_Link_State_Routing/
├── index.html          # Main HTML structure
├── script.js           # Core JavaScript logic and algorithms
├── style.css           # Styling and responsive design
├── README.md           # Project documentation
└── SPT_Optimization_in_Link_State_Routing.pptx  # Presentation slides
```

## 🚀 Getting Started

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- No additional software installation required

### Installation
1. **Clone or Download** the project files to your local machine
2. **Open** `index.html` in your web browser
3. **Start** building and testing your network topologies!

### Quick Start Guide
1. **Initialize Network**: Enter the number of routers and links
2. **Define Connections**: Specify which routers are connected and their costs
3. **Find Optimal Route**: Set source and destination routers
4. **Simulate Failures**: Test network resilience by marking routers as failed

## 📖 How to Use

### Step 1: Network Setup
- Enter the **Number of Routers** (minimum 1)
- Enter the **Number of Links** (minimum 1)
- Click **"Initialize Network"** to create the network structure

### Step 2: Define Connection Paths
- For each link, specify:
  - **Start Node**: Source router number
  - **End Node**: Destination router number  
  - **Weight**: Cost of the link (higher = more expensive)

### Step 3: Find Optimal Route
- Enter **Source Router** number
- Enter **Destination Router** number
- Click **"Show Link State Packets & Routing Tables"**

### Step 4: Simulate Router Failure (Optional)
- Enter the **Failed Router** number
- Click **"Mark Router as Failed"** to see how the network adapts

## 🔧 Technical Implementation

### Core Classes

#### `Node` Class
```javascript
class Node {
    constructor(val, cost) {
        this.val = val;        // Router identifier
        this.cost = cost;      // Link cost/weight
    }
}
```

#### `Graph` Class
```javascript
class Graph {
    constructor(numVertices) {
        this.numVertices = numVertices;
        this.adjList = Array.from({ length: numVertices + 1 }, () => []);
    }
    
    addEdge(start, end, weight)     // Add bidirectional link
    removeConnections(router)       // Remove failed router connections
}
```

### Key Algorithms

#### Dijkstra's Shortest Path Algorithm
- **Purpose**: Find shortest path from source to all destinations
- **Implementation**: Priority queue-based approach
- **Features**: Avoids failed routers, calculates both distances and previous nodes

#### Link State Packet (LSP) Generation
- **Purpose**: Simulate OSPF LSPs showing neighbor information
- **Content**: Neighbor router IDs and associated costs
- **Updates**: Automatically reflects router failures

#### Routing Table Construction
- **Purpose**: Generate complete routing tables for each router
- **Columns**: Destination, Next Hop, Total Cost
- **Features**: Handles unreachable destinations due to failures

## 🎯 Educational Value

This simulator is designed for:
- **Computer Networks Students**: Understanding link-state routing protocols
- **Network Engineers**: Visualizing OSPF behavior and troubleshooting
- **Educators**: Teaching routing concepts with interactive examples
- **Researchers**: Testing network resilience and optimization strategies

### Learning Objectives
- Understand how OSPF builds and maintains routing tables
- Learn about Shortest Path Tree (SPT) optimization
- Experience how networks adapt to router failures
- Visualize the difference between link-state and distance-vector routing

## 🌐 Network Visualization

The simulator uses **vis.js Network** to provide:
- **Interactive Graphs**: Click and drag to explore network topology
- **Color-coded Elements**: Failed routers and links are highlighted in red
- **Edge Labels**: Link costs are displayed on each connection
- **Responsive Layout**: Automatically adjusts to different screen sizes

## 🔍 Example Scenarios

### Basic Network Setup
```
Router 1 ←→ Router 2 (Cost: 5)
Router 2 ←→ Router 3 (Cost: 3)
Router 1 ←→ Router 3 (Cost: 8)
```

### Router Failure Simulation
- Mark Router 2 as failed
- Observe how Router 1 and Router 3 adapt their routing tables
- See the new optimal path: Router 1 → Router 3 (Cost: 8)

## 🎨 User Interface

### Design Features
- **Modern Gradient Background**: Professional blue-purple gradient
- **Card-based Layout**: Organized sections for different functions
- **Responsive Design**: Works on desktop, tablet, and mobile
- **Color Coding**: Intuitive visual feedback for different states
- **Clean Typography**: Easy-to-read fonts and spacing

### Interactive Elements
- **Form Validation**: Prevents invalid inputs
- **Real-time Updates**: Immediate visual feedback
- **Error Handling**: Clear error messages for invalid operations
- **Progressive Disclosure**: Features appear as needed

## 🚧 Future Enhancements

Potential improvements for future versions:
- **Multiple Algorithm Support**: Add Bellman-Ford and other routing algorithms
- **Network Load Simulation**: Test performance under different traffic loads
- **Advanced Failure Modes**: Simulate link failures, partial failures
- **Export Functionality**: Save network configurations and results
- **Animation Support**: Show step-by-step algorithm execution
- **Performance Metrics**: Display convergence time and efficiency metrics

## 🤝 Contributing

This project is open for educational use and contributions. Areas where contributions are welcome:
- **Algorithm Improvements**: Optimize existing algorithms or add new ones
- **UI/UX Enhancements**: Improve user interface and experience
- **Documentation**: Add more detailed explanations and examples
- **Testing**: Add comprehensive test cases and validation
- **Features**: Implement new simulation capabilities

## 📚 References

- **OSPF Protocol**: RFC 2328 - OSPF Version 2
- **Dijkstra's Algorithm**: Classic shortest path algorithm
- **Link State Routing**: Computer networking fundamentals
- **vis.js Documentation**: https://visjs.org/docs/network/

## 📄 License

This project is created for educational purposes. Feel free to use, modify, and distribute for learning and teaching network routing concepts.

## 👨‍💻 Author

Created as an educational tool for demonstrating Shortest Path Tree optimization in Link State Routing protocols.

---

**Happy Learning!** 🎓

*Explore the fascinating world of network routing and discover how modern networks find the most efficient paths for data transmission.*
