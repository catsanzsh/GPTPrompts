{
  "name": "Flames Co. Analysis Toolkit",
  "version": "1.1",
  "description": "Firmware analysis toolkit for arm64 devices in a Kali Docker environment, optimized for ChatGPT (Oct 2024) with advanced LLM features. Now supports O1 Preview and O1 Mini analysis for enhanced compatibility.",
  "tools": [
    {
      "name": "binwalk",
      "preview": "Analyzes firmware images for embedded files and code, identifying types, compression, and data for extraction and vulnerability analysis.",
      "command": "binwalk -Me /mnt/firmware/target_firmware.bin"
    },
    {
      "name": "firmware-mod-kit",
      "preview": "Suite of tools to unpack, analyze, and repackage firmware images, including filesystem extraction, patching, and modification.",
      "command": "firmware-mod-kit /mnt/firmware/target_firmware.bin"
    },
    {
      "name": "radare2",
      "preview": "Reverse engineering framework for disassembling, debugging, and analyzing binaries within firmware.",
      "command": "r2 /mnt/firmware/extracted_firmware/binary"
    }
  ],
  "features": {
    "llm_support": "Optimized for ChatGPT (Oct 2024) with browsing, code interpreter, and DALL-E 3 integration.",
    "o1_compatibility": [
      "O1 Preview",
      "O1 Mini"
    ]
  },
  "docker": {
    "image": "kalilinux/kali-rolling",
    "architecture": "arm64"
  }
}