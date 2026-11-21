# 📝 Worksheet: 03 - Strings and Text

Use this worksheet to reinforce your understanding of strings — creating them, slicing them, cleaning them up, and formatting them. Each section ends with an **🤖 Explain It** prompt — write your explanation in your own words, then (optionally) paste it into an AI tutor and ask it to point out anything you got wrong or left out.

---

## 🧠 Section 1: String Basics

1. Why doesn't Python care whether you use `'...'` or `"..."`?  
   `Answer:` ____Because they both create strings___________________

2. What's the output of this code?

```python
word = 'science'
print(word[0:3])
```

   `Answer:` ________sci_______________

3. Rewrite this string so it could be written with single quotes on the outside instead of double:

```python
message = "She said \"don't stop\""
```

   `Answer:` ___message = 'She said "don\'t stop"'____________________

---

### ✏️ Task: Slicing Practice

```python
# Given: course = "Programming for Data Science"
# Print just the word "Data" using slicing.
# Print the string reversed.

ourse = "Programming for Data Science"

print(course[17:21])

print(course[::-1])

```

### ✏️ Task: Multi-Line String

```python
# Write a triple-quoted string containing a 3-line "About Me" bio.
# Print it.

about_me = """My name is Katherine.
I am Senior at MSU Texas.
I work as a Project Engineer."""

print(about_me)

```

### 🤖 Explain It

In your own words: why are strings immutable, and what do you actually have to do if you want a "modified" version of a string?

They are immutable because you cannot change them after they're created. To modify them, you have to use .replace() or .strip()
---

## 🔁 Section 2: String Methods

4. What's the difference between `.strip()` and `.replace(' ', '')`?  
   `Answer:` ___strip removes spaces at beginning and end, and replace removes all spaces in the string ____________________

5. What will this print?

```python
name = "  ADA lovelace  "
print(name.strip().title())
```

   `Answer:` ____Ada Lovelace___________________

6. If `words = "red,green,blue".split(',')`, what is `words`, and what type is it?  
   `Answer:` _____it is a list__________________

---

### ✏️ Task: Clean and Validate

```python
# Given: raw_input = "  YES  "
# Clean it up (strip + lowercase) and check if it equals "yes".
# Print True or False.

raw_input = "  YES  "

cleaned = raw_input.strip().lower()

print(cleaned == "yes")

```

### ✏️ Task: Build a Sentence

```python
# Given: words = ['data', 'science', 'is', 'fun']
# Use .join() to turn this into the sentence "data science is fun".
# Then use .replace() to change "fun" to "powerful" in the result.

words = ['data', 'science', 'is', 'fun']

sentence = ' '.join(words)
print(sentence)

new_sentence = sentence.replace('fun', 'powerful')
print(new_sentence)

```

### 🤖 Explain It

In your own words: what's the difference between a method like `.upper()` that returns a new string, versus a list method like `.append()` that changes the list in place? Why do strings only work the first way?

Upper creates and returns a new string without change, append adds it to an existing list
---

## 🎯 Section 3: Formatted Strings

7. What does the format spec `:.2f` do?  
   `Answer:` ____It formats the number as a decimal with two numbers after decimal point___________________

8. What will this print?

```python
item = "eraser"
qty = 5
print(f"You bought {qty} {item}(s)")
```

   `Answer:` _____You bought 5 eraser(s)__________________

9. Why might you use an f-string instead of `+` to build a string out of variables?  
   `Answer:` ____f-strings make combining text and variables easier___________________

---

### ✏️ Task: Formatted Receipt

```python
# Given: item = "Backpack", price = 45.999, qty = 2
# Print a line like: "2x Backpack @ $46.00 = $92.00"
# (Notice price needs rounding — that's what :.2f is for.)

item = "Backpack"
price = 45.999
qty = 2

print(f"{qty}x {item} @ ${price:.2f} = ${price * qty:.2f}")

```

### ✏️ Task: Aligned Table

```python
# Given: names = ["Ana", "Bartholomew", "Cy"]
# Print each name right-aligned in a 15-character field, one per line,
# so they all line up on the right edge.

names = ["Ana", "Bartholomew", "Cy"]

for name in names:
    print(f"{name:>15}")

```

### 🤖 Explain It

In your own words: what's the practical difference between `f'{price}'` and `f'{price:.2f}'` when `price = 19.999999`? When would the difference actually matter in real code?

f'{price} displays 19.999999bbut f'{price:.2f} rounds it to two decimal places and to 20.00
---

## 🚀 Section 4: Going Further (Optional)

These pair with the "🔥 Challenge" sections in the notebooks — skip if you haven't gotten there yet.

### ✏️ Task: Raw String

```python
# Write the Windows path C:\Users\you\Desktop\notes.txt as a raw string.
# Print it, and explain in a comment why the plain (non-raw) version would be risky.

path = r"C:\Users\you\Desktop\notes.txt"

print(path)

```

### ✏️ Task: Debug Format Spec

```python
# Given: width = 10, height = 4
# Use the f'{expr=}' debug spec to print both "width" and "width * height"
# with their values, without writing separate print() calls for each.

width = 10
height = 4

print(f'{width=}, {width * height=}')

```

---

## 🧾 Submit Checklist

- [ ] I created strings with single quotes, double quotes, and triple quotes.
- [ ] I indexed and sliced a string.
- [ ] I used at least three different string methods (`.strip()`, `.split()`, `.join()`, `.replace()`, etc.).
- [ ] I built an f-string with more than one embedded expression.
- [ ] I used a format spec to control decimal places or alignment.
- [ ] I completed the "Explain It" prompts in my own words.
