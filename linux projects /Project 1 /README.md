# Linux Assignment-01 README

---

1. Check your current working directory
pwd


`
pwd prints the present working directory.
`

---

2. Create a directory "linux" in the current directory


`
mkdir linux
`

---

3. Create "Assignment-01" inside "linux"


`
mkdir linux/Assignment-01
`

---

4. Create "dir1" inside /tmp without changing current directory


`
mkdir /tmp/dir1
`

---

5. Create directories dir2 and dir3 inside /tmp/dir1 using a single command


`
mkdir -p /tmp/dir1/dir2 /tmp/dir1/dir3
`
-p ensures the parent directories are created if they don’t exist.

---

6. Delete "dir3"


`
rmdir /tmp/dir1/dir3
`
rmdir deletes an empty directory.

---

7. Create an empty file with your first name in /tmp


`
touch /tmp/first-name
`

---

8. Add first line without using an editor


`
echo "This is my first line" > /tmp/first-name
`

> creates or overwrites a file.

---

9. Add another line without overwriting


`
echo "This is additional content" >> /tmp/first-name
`

>> appends to the file.

---

10. Create a file with last name and some content


`
echo "last-name is my last name" > /tmp/last-name
`

---

11. Add a line at the beginning without an editor


`
echo "this is line at the beginning" | cat - /tmp/last-name > /tmp/last-name.tmp && mv /tmp/last-name.tmp /tmp/last-name
`

cat - file combines stdin (-) with the existing file. mv replaces the original.

---

12. Add 8-10 more lines


`
echo -e "line1\nline2\nline3\nline4\nline5\nline6\nline7\nline8\nline9\nline10" >> /tmp/last-name
`

-e enables interpreting \n as newline.

---

13. Display specific parts of the file
**Top 5 lines**
`
head -n 5 /tmp/last-name
`
---

**Bottom 2 lines**
`
tail -n 2 /tmp/last-name
`

---
 
 **Only 6th line**
`
sed -n '6p' /tmp/last-name
`

---

**Lines 3-8**
`
sed -n '3,8p' /tmp/last-name
`

---

14. List /tmp content
 **All content including hidden**
`
ls -a /tmp
`

---

**Only files**
`
find /tmp -maxdepth 1 -type f
`

---

**Only directories**
`
find /tmp -maxdepth 1 -type d
`

---

15. Copy "last-name" to /tmp/dir2
`
cp /tmp/last-name /tmp/dir1/dir2/
`

---

16. Copy with a different name
`
cp /tmp/last-name /tmp/dir1/dir2/last-name.copy
`

---

17. Rename "first-name" file
`
mv /tmp/first-name /tmp/new-first-name
`

---

18. Move "last-name" to /tmp/dir1
`
mv /tmp/last-name /tmp/dir1/
`

---

19. Clear content of /tmp/dir2/last-name.copy
`
         > /tmp/dir1/dir2/last-name.copy
`

> truncates the file, removing all content.

---

20. Delete /tmp/dir2/last-name.copy
`
rm /tmp/dir1/dir2/last-name.copy
`

✅ Assignment completed successfully.
