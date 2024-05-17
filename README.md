# EuclideanDistance
Calculate Euclidean distance between points
import math

# 1. Noktaların Tanımlanması
points = [
    (1, 2),
    (4, 6),
    (5, 8),
    (3, 7)
]

# 2. Öklid Mesafesi İçin Fonksiyon Yazma
def euclideanDistance(point1, point2):
    x1, y1 = point1
    x2, y2 = point2
    return math.sqrt((x2 - x1) ** 2 + (y2 - y1) ** 2)

# 3. Mesafelerin Hesaplanması
distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        distance = euclideanDistance(points[i], points[j])
        distances.append(distance)

# 4. Minimum Mesafenin Bulunması
min_distance = min(distances)
print("Minimum mesafe:", min_distance)
