import math, matplotlib.pyplot as plt


def est_premier(n):
    if n < 2 or (n % 2 == 0 and n != 2):
        return False

    else:
        for k in range(3, int(math.sqrt(n)) + 1, 2):
            if n % k == 0:
                return False
        else:
            return True


def liste_premier(n):
    L = []
    k = 1
    compteur = 0
    while compteur < n:
        k += 1
        if est_premier(k):
            L.append(k)
            compteur += 1

    return L


x = []
y = []


def majoration_pi_x_sur_x(L):
    produit = 1
    for k in range(len(L)):
        produit = produit * ((L[k] - 1) / L[k])

        x.append(k)
        y.append(produit)

    return produit


f = open("./10000000.txt")

N = 664579

list_premier = f.readlines()[:N]


for i in range(len(list_premier)):
    list_premier[i] = int(list_premier[i][: len(list_premier[i]) - 1])

print(majoration_pi_x_sur_x(list_premier))


fig, ax = plt.subplots(figsize=(20, 10))


ax.set_xlim(0, N)
ax.set_ylim(0, 1)


ax.set_title("Majoration de pi(x)/x en fonction de n")
ax.set_xlabel("n")
ax.set_ylabel("Majoration de pi(x)/x")


ax.plot(x, y)


plt.show()
