import os

# Split text by parts
part1 = "𝜗ৎ 𝖇𝖊𝖘𝖙 𝖋𝖗𝖎𝖊𝖓𝖉"
part2 = " / ℑ𝔱 𝔦𝔰 𝔞 𝔭𝔩𝔞𝔱𝔬𝔫𝔦𝔠 𝔯𝔢𝔩𝔞𝔱𝔦𝔬𝔫𝔰𝔥𝔦𝔭 𝔡𝔢𝔣𝔦𝔫𝔢𝔡 𝔟𝔶 𝔲𝔫𝔴𝔞𝔳𝔢𝔯𝔦𝔫𝔤 𝔩𝔬𝔶𝔞𝔩𝔱𝔶, 𝔪𝔲𝔱𝔲𝔞𝔩 𝔯𝔢𝔰𝔭𝔢𝔠𝔱, 𝔞𝔫𝔡 𝔢𝔪𝔬𝔱𝔦𝔬𝔫𝔞𝔩 𝔰𝔞𝔣𝔢𝔱𝔶"

# Convert HEX to RGB ANSI escape codes
# #cf1b53 -> R:207, G:27, B:83
# #d4a65e -> R:212, G:166, B:94
COLOR_BESTFRIEND = "\033[38;2;207;27;83m"
COLOR_REST = "\033[38;2;212;166;94m"
RESET = "\033[0m"

# Get terminal width for centering
try:
    terminal_width = os.get_terminal_size().columns
except OSError:
    terminal_width = 80

# Combine the raw text to calculate the correct alignment padding
full_raw_text = part1 + part2
padding = (terminal_width - len(full_raw_text)) // 2
spaces = " " * max(0, padding)

# Assemble with colors applied
colored_output = f"{spaces}{COLOR_BESTFRIEND}{part1}{COLOR_REST}{part2}{RESET}"

print(colored_output)


<img width="684" height="684" alt="krbkkidstintedcroppedandtexturednobg" src="https://github.com/user-attachments/assets/392b1828-4ea2-4f85-b6c3-5b25dbe87894" />

