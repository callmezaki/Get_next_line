# Get_next_line

## Description

The Get_next_line project involves implementing a function that reads from a file descriptor and returns a line of text until the end of the file. This project helps improve understanding of file I/O operations and dynamic memory allocation in C.

## Features

- Reads text from a file descriptor line by line
- Handles different buffer sizes
- Supports both single and multiple file descriptors

## Getting Started

### Prerequisites

- GCC or any C compiler
- Make

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/callmezaki/Get_next_line.git
   cd Get_next_line
   ```

2. Compile the project:

   ```bash
   make
   ```

### Usage

Include the `get_next_line` function in your project:

```c
#include "get_next_line.h"
```

Example usage:

```c
int fd = open("file.txt", O_RDONLY);
char *line;
while ((line = get_next_line(fd)) != NULL) {
    printf("%s\n", line);
    free(line);
}
close(fd);
```

## Project Structure

- `get_next_line.c`: Core function implementation.
- `get_next_line.h`: Header file.
- `get_next_line_utils.c`: Utility functions.
- `get_next_line_bonus.c`: Bonus part for handling multiple file descriptors.
- `get_next_line_bonus.h`: Header file for the bonus part.
- `Makefile`: Defines the build process for the project.
- `README.md`: Project documentation.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any changes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [42 School](https://42.fr/en/homepage/) for providing the project framework.
- The 42 community for their support and collaboration.
