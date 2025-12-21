# Claude Code Plugin Collection

A collection of useful plugins for Claude Code CLI, focusing on translation and text processing capabilities.

## Features

### Translation Commands

- **`/to-ch`** - Translate text to Traditional Chinese
- **`/to-en`** - Translate text to English

Both commands maintain technical terminology accuracy during translation.

## Installation

### Local Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/claude-code-plugin.git
cd claude-code-plugin
```

2. Install the plugin to Claude Code:
```bash
claude plugin add ./
```

### NPM Installation (Coming Soon)

```bash
claude plugin add @ry/claude-code-plugins
```

## Usage

### Translate to Chinese

```bash
claude /to-ch "Hello, World! This is a technical document."
```

Output:
```
你好，世界！這是一個技術文件。
```

### Translate to English

```bash
claude /to-en "這是一個測試訊息，包含技術術語。"
```

Output:
```
This is a test message containing technical terminology.
```

## Plugin Structure

```
claude-code-plugin/
├── plugin.json          # Plugin configuration
├── commands/            # Command definitions
│   ├── to-ch.md        # Chinese translation prompt
│   └── to-en.md        # English translation prompt
├── package.json         # NPM package configuration
├── README.md           # This file
├── LICENSE             # MIT License
├── .gitignore          # Git ignore rules
└── .npmignore          # NPM ignore rules
```

## Development

### Adding New Commands

1. Create a new prompt file in `commands/` directory:
```bash
touch commands/your-command.md
```

2. Add command definition to `plugin.json`:
```json
{
  "name": "your-command",
  "description": "Command description",
  "prompt": "commands/your-command.md"
}
```

3. Test the command:
```bash
claude /your-command "test input"
```

### Testing

```bash
npm run validate
```

## Requirements

- Claude Code CLI >= 0.1.0
- Node.js >= 18.0.0

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Author

RY

## Changelog

### v1.0.0 (2025-12-21)
- Initial release
- Added Chinese translation command (`/to-ch`)
- Added English translation command (`/to-en`)

## Support

If you encounter any issues or have questions, please [open an issue](https://github.com/yourusername/claude-code-plugin/issues).

## Related Links

- [Claude Code Documentation](https://docs.anthropic.com/claude/docs)
- [Plugin Development Guide](https://docs.anthropic.com/claude/docs/plugins)
