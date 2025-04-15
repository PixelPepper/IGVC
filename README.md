# IGVC (Intelligent Ground Vehicle Competition) ROS Project

This repository contains the ROS (Robot Operating System) workspace for the Intelligent Ground Vehicle Competition project. It utilizes NVIDIA's Isaac ROS Common packages for robotics development.

## Prerequisites

- Ubuntu 22.04
- ROS 2 (Humble)
- NVIDIA GPU (recommended)
- Git
- Docker (optional, for containerized development)

## Installation

### 1. Clone the Repository

Clone this repository with its submodules using:

```bash
git clone --recursive https://github.com/PixelPepper/IGVC.git
cd IGVC
```

If you already cloned the repository without `--recursive`, initialize the submodules with:

```bash
git submodule update --init --recursive
```

### 2. Setup Isaac ROS Common

The `isaac_ros_common` package is included as a submodule and provides essential functionality for working with NVIDIA's Isaac ROS packages. It will be automatically downloaded when cloning recursively.

### 3. Build the Workspace

```bash
cd isaac_ros-dev
colcon build --symlink-install
```

### 4. Source the Workspace

```bash
source install/setup.bash
```

Add this to your `~/.bashrc` to make it permanent:

```bash
echo "source ~/path/to/IGVC/isaac_ros-dev/install/setup.bash" >> ~/.bashrc
```

## Project Structure

```
IGVC/
├── isaac_ros-dev/          # Main ROS 2 workspace
│   ├── src/               # Source directory
│   │   └── isaac_ros_common/  # NVIDIA Isaac ROS common packages (submodule)
│   ├── build/             # Build artifacts (generated)
│   ├── install/           # Installation files (generated)
│   └── log/               # Log files (generated)
└── README.md              # This file
```

## Development

### Building the Project

To build all packages in the workspace:

```bash
cd isaac_ros-dev
colcon build --symlink-install
```

To build a specific package:

```bash
colcon build --packages-select package_name
```

### Running Tests

```bash
colcon test
colcon test-result --verbose
```

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the [MIT License](LICENSE) - see the LICENSE file for details.

## Acknowledgments

- NVIDIA Isaac ROS team for providing the [isaac_ros_common](https://github.com/NVIDIA-ISAAC-ROS/isaac_ros_common) packages
- ROS 2 community for the robotics framework

## Contact

Your Name - [@YourTwitter](https://twitter.com/YourTwitter)

Project Link: [https://github.com/PixelPepper/IGVC](https://github.com/PixelPepper/IGVC) 
