# func
functiom 
def applyEachTo(L, x):
    result = []
    for i in range(len(L)):
        result.append(L[i](x))
    return result

def square(a):
    return a * a


def halve(a):
    return a / 2


def inc(a):
    return a + 1

print(inc(7))
print(applyEachTo([inc], 9))
print(applyEachTo([inc, square, halve, abs], -3))


def applyToEach_fuc(L, f):
    for i in range(len(L)):
        L[i] = f(L[i])
    return L

L =[5,-3,6]

f = square
print(applyToEach_fuc(L, f))
