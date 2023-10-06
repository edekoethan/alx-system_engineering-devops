grep Command:
grep is a powerful command-line tool for searching and matching patterns in text files. You can use it with regular expressions as follows:

bash
Copy code
grep "pattern" file.txt
For example, to search for all lines containing the word "apple" in a file:

bash
Copy code
grep "apple" file.txt
You can use regular expressions to match more complex patterns. For instance, to find lines containing "apple" or "banana," you can use the | (OR) operator:

bash
Copy code
grep "apple\|banana" file.txt
sed Command:
sed (stream editor) is a command-line utility for text processing and manipulation. It allows you to use regular expressions to perform substitutions, deletions, and other operations on text.

To use sed with regex, you typically specify a pattern and the replacement text:

bash
Copy code
sed 's/pattern/replacement/' file.txt
For example, to replace all occurrences of "apple" with "orange" in a file:

bash
Copy code
sed 's/apple/orange/' file.txt
Regular expressions can be used in the pattern part to perform more advanced text transformations.

[[ and =~ Operators:
In Bash, you can use the [[ operator along with the =~ operator to perform regex matching directly in conditional statements:

bash
Copy code
if [[ "$string" =~ regex_pattern ]]; then
    # code to execute if the string matches the pattern
fi
For example, checking if a string is a valid email address:

bash
Copy code
email="example@email.com"
if [[ "$email" =~ ^[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,4}$ ]]; then
    echo "Valid email address."
else
    echo "Invalid email address."
fi
awk Command:
awk is a versatile text processing tool that allows you to specify actions based on patterns. You can use regex patterns in awk to match and process specific parts of input data.

For instance, to print all lines where the second field contains the word "apple" or "banana":

bash
Copy code
awk '$2 ~ /apple|banana/' file.txt
