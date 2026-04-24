# RPG-character
project
def create_character(name, strength, intelligence, charisma):
    if not isinstance(name, str):
        return 'The character name should be a string'
    elif name == "":
        return 'The character should have a name'
    elif len(name) > 10:
        return 'The character name is too long'
    elif " " in name:
        return 'The character name should not contain spaces'
    elif not (isinstance(strength, int) and isinstance(intelligence, int) and isinstance(charisma, int)):
        return 'All stats should be integers'
    elif strength < 1 or intelligence < 1 or charisma < 1:
        return 'All stats should be no less than 1'
    elif strength > 4 or intelligence > 4 or charisma > 4:
        return 'All stats should be no more than 4'
    elif (strength + intelligence + charisma) != 7:
        return 'The character should start with 7 points'

    
    str_bar = '●'* strength + '○'* (10 - strength)
    int_bar = '●'* intelligence + '○'* (10 - intelligence)
    cha_bar = '●'* charisma + '○'* (10 - charisma)

    return f"{name}\nSTR {str_bar}\nINT {int_bar}\nCHA {cha_bar}"

