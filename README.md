# Bulk_Watermarker_Python

**Bulk_Watermarker_Python** is a simple and efficient Python utility to **batch watermark images with custom text**.  
It processes an entire folder of images and applies a clean text watermark automatically.

---

## Features

- Bulk watermarking of images in a folder
- Supports formats: **JPG, JPEG, PNG, BMP**
- Custom watermark text
- Adjustable font size
- Automatic bottom-right watermark positioning
- Creates output directory automatically
- Preserves original images (non-destructive)

---

## Tech Stack

- Python 3
- Pillow (PIL)
- OS module

---

## Project Structure

```
Bulk_Watermarker_Python/
│
├── input_dir/          # Place original images here
├── output_dir/         # Watermarked images will be saved here
├── watermark.py        # Main script
├── super_nought.ttf    # Custom font file
└── README.md
```

---

## Installation

### 1. Clone the repository
```bash
git clone https://github.com/your-username/Bulk_Watermarker_Python.git
cd Bulk_Watermarker_Python
```

### 2. (Optional) Create virtual environment
```bash
python -m venv watermark
watermark\Scripts\activate
```

### 3. Install dependencies
```bash
pip install pillow
```

---

## Usage

1. Put your images into the `input_dir` folder

2. Run the script:

```bash
python watermark.py
```

3. Get results inside:

```
output_dir/
```

---

## Configuration

Edit inside `watermark.py`:

```python
input_directory = "./input_dir"
output_directory = "./output_dir"
watermark_text = "@Daksh"
font_size = 299
```

---

## Custom Font

The script uses a `.ttf` font:

```python
ImageFont.truetype("super_nought.ttf", size=font_size)
```

Ensure:
- The font file exists in the project root  
OR  
- Provide absolute font path

---

## How It Works

- Loads each image using Pillow
- Calculates text dimensions dynamically
- Positions watermark at bottom-right corner
- Draws watermark text
- Saves new image in output folder

---

## Example Output

```
input_dir/
 ├── img1.jpg
 ├── img2.png

output_dir/
 ├── watermarked_img1.jpg
 ├── watermarked_img2.png
```

---

## Notes

- Original images are **not modified**
- Output images are saved with prefix:

```
watermarked_<original_filename>
```

---

## Future Improvements

- Transparent / opacity watermark
- Logo/image watermark support
- Custom positions (center, top-left, tiled)
- CLI arguments
- GUI version (Tkinter or Electron)

---

## Contributing

Pull requests are welcome. For major changes, please open an issue first.

---

## License

MIT License

---

## Author

**Daksh**
