# Number-Picking-Game

In a mystical land, two friends, Arjun and Neha, are playing an exciting game with a list of N magical numbers. Both start with own list containing the same numbers but have different strategies for selecting them. Arjun always picks a number from the start of his list, while Neha picks from the end of hers.
The game has simple rules:
If Arjun’s number is greater than Neha’s, the outcome is 1, and Neha removes her number from the list.
If Arjun’s number is smaller than Neha’s, the outcome is 2, and Arjun removes his number.
If they both pick the same number, the outcome is 0, and both remove their numbers.
The game continues until at least one of them runs out of numbers to pick. Can you determine the sequence of outcomes as they play this game?

x = int(input())
a = list(map(int, input().split()))
n = list(a)
l = []
while a and n:
    if a[0]>n[-1]:
        n.pop()
        l.append(1)
    elif a[0]<n[-1]:
        a.pop(0)
        l.append(2)
    else:
        a.pop(0)
        n.pop()
        l.append(0)
print(*l)
