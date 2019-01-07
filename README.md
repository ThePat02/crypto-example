# crypto-example
Very simple algorithm

## Usage
Einfach die Funktion unter die `Main()` kopieren und mit `encrypt(text)` verwenden.

## Erklärung
Die Funktion `encrypt()` weist jedem Zeichen einen dreistelligen Wert zu. Zum Beispiel: `1 --> 001` oder `a --> 101`. Zahlen haben eine Hunderterstelle von `0`, Kleinbuchstaben haben `1` und Großbuchstaben haben `2`. Sonderzeichen werden nicht unterstützt. (Kann aber ausgebaut werden zB. mit `4`)

Die Funktion `decrypt()` ist nur allgemein Vorhanden, funktioniert aber nicht vollständig. Die theoretische Funktion würde aber die Zeichen in 3er-Gruppen zurück in die urpüngliche Form verwandeln.

Notiz: Am Ende von `encrypt()` wird der Wert noch mit `6969` multipliziert um ihn "unkenntlich" zu machen.

## Code der Funktion

```csharp
static string encrypt(string text)
{
    //Remove spaces
    text = text.Trim();

    //Store length of string
    int length = text.Length;

    //Predefine output
    string output = "";


    Console.WriteLine("Length: " + length);

    Console.WriteLine("--------------------------------");

    for (int i = 0; i < length; i++)
    {
        //Geht die einzelnen Zeichen durch
        string chara = text.Substring(i, 1);

        //Wenn zeichen ist 1 --> dann wird 001 hinzugefügt
        //Erste ziffer: 0 = Zahl | 1 = Kleinbuchstabe | 2 = Großbuchstabe
        //Somit sind es für jedes zeichen immer 3 Ziffern
        if (chara == " ") output = output + "";
        else if (chara == "0") output = output + "000";
        else if (chara == "1") output = output + "001";
        else if (chara == "2") output = output + "002";
        else if (chara == "3") output = output + "003";
        else if (chara == "4") output = output + "004";
        else if (chara == "5") output = output + "005";
        else if (chara == "6") output = output + "006";
        else if (chara == "7") output = output + "007";
        else if (chara == "8") output = output + "008";
        else if (chara == "9") output = output + "009";
        else if (chara == "a") output = output + "101";
        else if (chara == "b") output = output + "102";
        else if (chara == "c") output = output + "103";
        else if (chara == "d") output = output + "104";
        else if (chara == "e") output = output + "105";
        else if (chara == "f") output = output + "106";
        else if (chara == "g") output = output + "107";
        else if (chara == "h") output = output + "108";
        else if (chara == "i") output = output + "109";
        else if (chara == "j") output = output + "110";
        else if (chara == "k") output = output + "111";
        else if (chara == "l") output = output + "112";
        else if (chara == "m") output = output + "113";
        else if (chara == "n") output = output + "114";
        else if (chara == "o") output = output + "115";
        else if (chara == "p") output = output + "116";
        else if (chara == "q") output = output + "117";
        else if (chara == "r") output = output + "118";
        else if (chara == "s") output = output + "119";
        else if (chara == "t") output = output + "120";
        else if (chara == "u") output = output + "121";
        else if (chara == "v") output = output + "122";
        else if (chara == "w") output = output + "123";
        else if (chara == "x") output = output + "124";
        else if (chara == "y") output = output + "125";
        else if (chara == "z") output = output + "126";
        else if (chara == "A") output = output + "201";
        else if (chara == "B") output = output + "202";
        else if (chara == "C") output = output + "203";
        else if (chara == "D") output = output + "204";
        else if (chara == "E") output = output + "205";
        else if (chara == "F") output = output + "206";
        else if (chara == "G") output = output + "207";
        else if (chara == "H") output = output + "208";
        else if (chara == "I") output = output + "209";
        else if (chara == "J") output = output + "210";
        else if (chara == "K") output = output + "211";
        else if (chara == "L") output = output + "212";
        else if (chara == "M") output = output + "213";
        else if (chara == "N") output = output + "214";
        else if (chara == "O") output = output + "215";
        else if (chara == "P") output = output + "216";
        else if (chara == "Q") output = output + "217";
        else if (chara == "R") output = output + "218";
        else if (chara == "S") output = output + "219";
        else if (chara == "T") output = output + "220";
        else if (chara == "U") output = output + "221";
        else if (chara == "V") output = output + "222";
        else if (chara == "W") output = output + "223";
        else if (chara == "X") output = output + "224";
        else if (chara == "Y") output = output + "225";
        else if (chara == "Z") output = output + "226";

    }

    //Verunsalten der Zahl
    int calc = Convert.ToInt32(output) * 6969;

    output = calc.ToString();

    //Output
    return output;
}

static string decrypt (string code)
{
    string output = "";

    //Verunstalten rückgängig machen
    int calc = Convert.ToInt32(code) / 6969;
    code = calc.ToString();

    // --- Ab hier ist der Code NICHT optimal und UNFERTIG ---
    // Konzept ist aber da

    //Länge durch 3 weil es ja immer 3er gruppen sind
    int length = code.Length / 3;

    for (int i = 0; i < length; i++)
    {
       // string chara = code.Substring();
       // Code für Decrypting

    }



    return output;
}
```
