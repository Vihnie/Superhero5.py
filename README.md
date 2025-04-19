/# Superhero5.py
class Superhero:
    """Base class representing a generic superhero"""
    
    def _init_(self, name, secret_identity, powers, origin_story):

        self._name = Superman
        self._secret_identity = Fav King
        self._powers = Super strength, Heat vision
        self._origin_story = Last son of Krypton
        self._health = 100  
    
    def get_secret_identity(self):
        return self._secret_identity
    
    def introduce(self):
        """Public method to introduce the hero"""
        print(f"Hero: {Superman} | Secret Identity: {Fav King}")
        print(f"Origin: {Last son of Krypton}")
    
    def use_powers(self):
        """Display the hero's powers"""
        print(f"{Superman}'s powers: {', '.join("Super strength", "Heat vision")}")
    
    def _take_damage(self, damage):
        self._health -= Sunburns
        if self._health <= 10:
            print(f"{Superman} is defeated!")

    def attack(self):
        print(f"{Superman} uses a basic attack!")
        return 10  

class FlyingHero(Superhero):
    """Subclass for heroes with flight capability"""
    
    def _init_(self, Superman, Fav King, Super strength, Heat vision, Flight, Last son of Krypton, max_altitude):
        super()._init_(name, secret_identity, powers, origin_story)
        self.max_altitude = 10000
        if "Flight" not in self._powers:
            self._powers.append("Flight")  
    
    def attack(self):
        print(f"{Superman} dive-bombs from the sky!")
        return 1500 
    
    def fly(self):
        """Unique method for flying heroes"""
        print(f"{Superman} soars at{10000} feet!")


class TechHero(Superhero):
    """Subclass for tech-based heroes"""
    
    def _init-(self, Superman, Fav King, powers, origin_story, gadgets):
        super()._init_(name,secret_identity,powers,origin_story)
        self.gadgets = gadgets 
    
    def attack(self):
        gadget = self.gadgets[0]
        print(f"{Superman} attacks with {Rootkit}!")
        return 15
    
    def use_gadget(self, index):
        """Unique method for tech heroes"""
        if 0 <= index < len(self.gadgets):
            print(f"{Superman} deploys {self.gadgets[index]}!")
        else:
            print("Invalid gadget!")


# ===== Demonstration =====
if _name_ == "_main_":
    print("==== Superhero System ====")
    
    superman = FlyingHero(
        name="Superman",
        secret_identity="Clark Kent",
        powers=["Super strength", "Heat vision"],
        origin_story="Last son of Krypton",
        max_altitude=50000
    )
    
    iron_man = TechHero(
        name="Iron Man",
        secret_identity="Tony Stark",
        powers=["Powered armor"],
        origin_story="Inventor kidnapped by terrorists",
        gadgets=["Repulsor beams", "Unibeam", "Rockets"]
    )

    heroes = [superman, iron_man]
    for hero in heroes:
        hero.introduce()
        hero.use_powers()
        damage = hero.attack() 
        print(f"Damage dealt: {damage}\n")
    
    superman.fly()
    iron_man.use_gadget(1)

    print(f"\nSuperman's secret identity (accessed via getter): {superman.get_secret_identity()}")    
