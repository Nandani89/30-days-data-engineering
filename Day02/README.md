# Day 02
# Day 2 – Linux and Shell Basics

This document contains **100 essential Linux commands for Data Engineering** with examples.  
Practice them daily to master Linux and Shell scripting.

---

## 📂 File & Directory Management
1. `pwd` → Print current directory  
   ```bash
   pwd
ls → List files
ls -l → Long listing with details
ls -lh → Human-readable file sizes
ls -a → Show hidden files
ls -lt → Sort by modified time
cd /path/to/dir → Change directory

cd .. → Go up one directory

cd - → Go to previous directory

mkdir project → Create directory

mkdir -p project/raw/csv → Create nested directories

rmdir emptydir → Remove empty directory

rm -r olddir → Remove directory recursively

touch file.txt → Create empty file

cp file1 file2 → Copy file

cp -r dir1 dir2 → Copy directory

mv file1 file2 → Move/Rename file

rm file.txt → Delete file

stat file.txt → Show file metadata

tree → Display directory structure

📄 File Viewing & Editing
cat file.txt → Print contents

tac file.txt → Print in reverse

head file.txt → Show first 10 lines

head -n 5 file.txt → Show first 5 lines

tail file.txt → Show last 10 lines

tail -n 5 file.txt → Show last 5 lines

tail -f app.log → Live monitor logs

less file.txt → Scroll inside file

more file.txt → View file page by page

nano file.txt → Edit with Nano editor

vi file.txt → Edit with Vi editor

strings binaryfile → Extract text from binary

🔍 Searching & Filtering
grep "error" logfile.txt → Find lines with error

grep -i "error" logfile.txt → Case insensitive search

grep -v "error" logfile.txt → Exclude matches

grep -r "error" logs/ → Recursive search

egrep "error|fail" logfile.txt → Multiple patterns

zgrep "error" file.gz → Search inside gzipped file

find . -name "*.csv" → Find CSV files

find . -type f -size +100M → Find files >100MB

locate passwd → Locate file quickly

which python3 → Show path of python3

whereis python3 → Show binary/docs/man pages

📊 File Processing
wc file.txt → Count lines, words, characters

wc -l file.txt → Count lines

wc -w file.txt → Count words

sort file.txt → Sort file alphabetically

sort -r file.txt → Reverse sort

sort -n numbers.txt → Numeric sort

uniq names.txt → Remove duplicates

uniq -c names.txt → Count duplicates

cut -d"," -f1 data.csv → Extract first column

cut -c 1-10 file.txt → Extract characters 1–10

awk '{print $1}' file.txt → Print first column

awk -F"," '{print $2}' data.csv → Print 2nd field

sed 's/error/failure/g' logfile.txt → Replace error→failure

sed -n '10,20p' file.txt → Show lines 10–20

paste file1 file2 → Merge line by line

join file1 file2 → Join on common field

split -l 1000 bigfile.txt chunk_ → Split large file

📦 Compression & Archiving
tar -cvf data.tar files/ → Create tar archive

tar -xvf data.tar → Extract tar

tar -czvf data.tar.gz files/ → Compress tar.gz

tar -xzvf data.tar.gz → Extract tar.gz

gzip file.txt → Compress file

gunzip file.txt.gz → Decompress file

zip archive.zip file1 file2 → Create zip

unzip archive.zip → Extract zip

⚙️ Permissions & Ownership
ls -l → Show permissions

chmod 644 file.txt → rw-r--r--

chmod 755 script.sh → rwxr-xr-x

chmod +x script.sh → Add execute permission

chown user file.txt → Change owner

chown user:group file.txt → Change owner & group

groups → Show groups

umask → Show default permission mask

⚡ Process & System Monitoring
ps → Show processes

ps aux → Show all processes

top → Real-time process monitor

htop → Better process monitor (if installed)

kill -9 <pid> → Kill process by PID

jobs → Show background jobs

bg %1 → Resume job in background

fg %1 → Bring job to foreground

df -h → Disk usage

du -sh * → Size of files/folders

free -h → Memory usage

uptime → System uptime

uname -a → System info

whoami → Current user

🌐 Networking
ping google.com → Test connectivity

curl http://example.com → Fetch webpage

wget http://example.com/file.csv → Download file

scp file.txt user@host:/path → Copy file over SSH

rsync -av source/ dest/ → Sync directories

netstat -tuln → List open ports

ss -tuln → Modern alternative to netstat

ifconfig → Show network config (legacy)

ip addr → Show network config (modern)

traceroute google.com → Trace route to host

