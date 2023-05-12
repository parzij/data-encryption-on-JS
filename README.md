```c++
let key = prompt("Введите ключ: ");

let message = prompt("Введите сообщение для шифрования: ");

let keyArray = []; for (let i = 0; i < key.length; i++) { keyArray.push(key.charCodeAt(i)); }

let encryptedMessage = ""; for (let i = 0; i < message.length; i++) { let charCode = message.charCodeAt(i);

let keyCharCode = keyArray[i % keyArray.length];

let encryptedCharCode = charCode ^ keyCharCode;

let encryptedChar = String.fromCharCode(encryptedCharCode);

encryptedMessage += encryptedChar;
}

alert("Зашифрованное сообщение: " + encryptedMessage);
```
