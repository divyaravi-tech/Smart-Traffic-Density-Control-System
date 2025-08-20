# Smart-Traffic-Density-Control-System
This project simulates a smart traffic system that adjusts green light duration based on the number of vehicles waiting at each signal.
#include <stdio.h>

int main() {
    int north, south, east, west;
    int totalVehicles;

    printf("=== Smart Traffic Density Control System ===\n");

    // Input vehicle count on each road
    printf("Enter number of vehicles at North road: ");
    scanf("%d", &north);
    printf("Enter number of vehicles at South road: ");
    scanf("%d", &south);
    printf("Enter number of vehicles at East road: ");
    scanf("%d", &east);
    printf("Enter number of vehicles at West road: ");
    scanf("%d", &west);

    totalVehicles = north + south + east + west;

    if (totalVehicles == 0) {
        printf("\n✅ No vehicles detected. All signals remain RED.\n");
        return 0;
    }

    printf("\n--- Signal Timings (Proportional to Traffic Density) ---\n");

    printf("🟢 North Signal Green Time: %d seconds\n", (north * 60) / totalVehicles);
    printf("🟢 South Signal Green Time: %d seconds\n", (south * 60) / totalVehicles);
    printf("🟢 East Signal Green Time: %d seconds\n", (east * 60) / totalVehicles);
    printf("🟢 West Signal Green Time: %d seconds\n", (west * 60) / totalVehicles);

    printf("\n✅ Smart traffic control completed.\n");

    return 0;
}
