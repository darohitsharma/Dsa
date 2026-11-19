# Linked-List and Binary-Search Exercises

`Dsa.ipynb` contains fourteen code cells with linked-list and search exercises, followed by an empty cell. It is coursework with known incomplete or incorrect cases, not a validated data-structure library.

## Contents

Linked-list snippets cover reversal, sorted merging, removal from the end, intersection, digit-list addition, pair swapping, k-group reversal, palindrome checks, rotation, multilevel flattening, odd/even rearrangement and incrementing a digit list. Final cells show insertion-position and rotated-array binary search.

`ListNode` and `Node` are redefined across cells. Examples mutate links and sometimes the input list itself. Read each snippet in its own context; do not assume all definitions form a shared stable API.

## Read locally

Open the notebook in Jupyter or a notebook-capable editor using Python 3. It uses built-in Python without an external dataset or service. Inspect cells before running them. Avoid an unattended run-all: a function can be syntactically valid yet loop or produce an incorrect result when called.

## Confirmed review findings

- `removeNthFromEnd` raises `AttributeError` for an index larger than the list length (reproduced on a one-node list with `n=3`).
- `reverseKGroup` did not terminate within a bounded check for two nodes and `k=2`; its loop can leave the current pointer unchanged. Do not treat it as ready to run on arbitrary inputs.
- `isPalindrome` returns `True` for the non-palindrome `[1, 2]` and changes links. The positive result is not a reliable correctness check.
- The included flattening example raises `AttributeError` during its list construction, before the flatten function can be validated.

These are targeted findings, not an exhaustive audit. Other routines and input domains are not certified correct. Search examples assume the ordering conditions described by their exercise; digit-list routines need a clearly understood digit order.

This update adds only documentation. Original functions, examples, saved outputs, names and git history are unchanged; no missing algorithm has been invented or silently replaced.
