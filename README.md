# Cr-a-Jardin-Paysagiste-Virtuel-par-IA-G-n-rative
Créa-Jardin utilise l'IA générative pour concevoir des aménagements paysagers personnalisés en fonction des préférences esthétiques, du climat et de l'espace disponible des utilisateurs.
import random

# Mock database of garden templates
garden_templates = {
    "tropical": {
        "small": "Tropical garden with small palms and colorful undergrowth.",
        "medium": "Medium tropical garden with a variety of palms, ferns, and flowers.",
        "large": "Large tropical paradise with tall palms, dense undergrowth, and a small pond."
    },
    "desert": {
        "small": "Small desert garden with succulents and cacti.",
        "medium": "Medium desert landscape with rocks, cacti, and aloe plants.",
        "large": "Large desert oasis with a variety of cacti, succulents, and a central water feature."
    },
    "woodland": {
        "small": "Cozy small woodland garden with ferns, small trees, and moss.",
        "medium": "Medium woodland setup with a mix of bushes, trees, and a small creek.",
        "large": "Large enchanted woodland garden with dense trees, a pond, and various plants."
    }
}

# Function to generate garden design based on user input
def generate_garden_design(preference, climate, space):
    try:
        # Select a garden template based on the user's preference and space
        garden_design = garden_templates[preference][space]
        return garden_design
    except KeyError:
        return "We couldn't find a garden design that matches your preferences. Please try again."

# Main program
if __name__ == "__main__":
    # Prompt user for their garden preferences
    print("Welcome to Créa-Jardin, your virtual landscaper powered by AI.")
    preference = input("What's your aesthetic preference? Choose tropical, desert, or woodland: ").lower()
    climate = input("What's your local climate like? This will help us make the best plant suggestions: ").lower()
    space = input("What's the size of your available space? Choose small, medium, or large: ").lower()

    # Generate garden design
    garden_design = generate_garden_design(preference, climate, space)

    # Output the generated garden design
    print("\nYour personalized garden design:")
    print(garden_design)
