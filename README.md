#projectkopi
with open("/mnt/data/website_bisnis/README.md", "w", encoding="utf-8") as f:
    f.write(readme_md.strip())

with open("/mnt/data/website_bisnis/.gitignore", "w", encoding="utf-8") as f:
    f.write(gitignore.strip())

# Tambahkan ke file ZIP
with ZipFile("/mnt/data/website_bisnis.zip", "a") as zipf:
    zipf.write("/mnt/data/website_bisnis/README.md", arcname="README.md")
    zipf.write("/mnt/data/website_bisnis/.gitignore", arcname=".gitignore")

"/mnt/data/website_bisnis.zip"
