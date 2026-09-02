# Bugs found

Add one section per issue. Bug 1 is filled in to show the format — fix it, then write what you changed. Copy the blank template for the rest.

Keep this file in the repo and **commit it** with your fixes.

---



## Bug 1

**How to reproduce**:

Add multiple expenses with different dates and Open the expense list and Observe the order of the expenses.

**What is wrong**:

The expenses are displayed from the oldest date to the newest date, even though the requirement says that expenses should be displayed with the newest expense first.

**What I changed**:

Changed the sorting logic to sort expenses by date in descending order so that the most recent expense appears first.

---
## Bug 2
**How to reproduce**:Add multiple expenses and Sort or filter the expense list,
Select an expense that is not in its original array position,Click Edit or Delete.observe which expense is modified or deleted.

**What is Wrong**:The UI uses the index of the sorted/filtered array when updating or deleting an expense. This index may not match the expense's index in the original expenses array.

**What I changed** :Changed the update and delete logic to use the expense's unique id instead of relying on the array index:
---
Bug 3: 

How to reproduce:

Add an expense paid by one member.
Split the expense between multiple members.
Open the balances section.
Check the balance message.

What is wrong:

A positive balance means the member should receive money, but the application displays that the member "owes" money. A negative balance means the member owes money, but the application displays that they "are owed" money.

What I changed:

Corrected the balance labels:

Positive balance → is owed
Negative balance → owe
---
Bug 4
How to reproduce:
Add an expense of $100,Split it equally between 3 people and Check each person's share,Add the shares together.

What is wrong:
$100 / 3 produces $33.333.... Rounding each share independently gives $33.33 + $33.33 + $33.33 = $99.99, which is one cent less than the original bill.

What I changed:
Changed the equal-split calculation so that rounding differences are distributed among the participants and the final shares always add up exactly to the original bill.



