UKRAINIAN_LOWER = 'абвгдеєжзишїйклмнопрстуфхцчшщьюя'
UKRAINIAN_UPPER = UKRAINIAN_LOWER.upper()


def encode(data, key=1):
    encode_data = ''
    for char in data:
        if char in UKRAINIAN_LOWER:
            encode_data += UKRAINIAN_LOWER[(UKRAINIAN_LOWER.index(char) + key) % len(UKRAINIAN_LOWER)]
        elif char in UKRAINIAN_UPPER:
            encode_data += UKRAINIAN_UPPER[(UKRAINIAN_LOWER.index(char) + key) % len(UKRAINIAN_UPPER)]
        else:
            encode_data += char
    return encode_data


def decode(data, key=1):
    decode_data = ''
    for char in data:
        if char in UKRAINIAN_LOWER:
            decode_data += UKRAINIAN_LOWER[(UKRAINIAN_LOWER.index(char) - key) % len(UKRAINIAN_LOWER)]
        elif char in UKRAINIAN_UPPER:
            decode_data += UKRAINIAN_UPPER[(UKRAINIAN_LOWER.index(char) - key) % len(UKRAINIAN_UPPER)]
        else:
            decode_data += char
    return decode_data


string = input("Введіть текст: ")
print(encode(string, 3))
