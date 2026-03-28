#include <iostream>
#include <string>
using namespace std;

class Colet {
private:
    string expeditor;
    string destinatar;
    float greutate;
    string adresa;
    string status;
    string dataLivrare;

public:
    Colet() {
        expeditor = "Necunoscut";
        destinatar = "Necunoscut";
        greutate = 0;
        adresa = "-";
        status = "Nelivrat";
        dataLivrare = "-";
    }

    Colet(string exped, string dest, float gr, string adr) {
        expeditor = exped;
        destinatar = dest;
        greutate = gr;
        adresa = adr;
        status = "Nelivrat";
        dataLivrare = "-";
    }

    Colet(const Colet& c) {
        expeditor = c.expeditor;
        destinatar = c.destinatar;
        greutate = c.greutate;
        adresa = c.adresa;
        status = c.status;
        dataLivrare = c.dataLivrare;
    }

    ~Colet() {
        cout << "Coletul pentru destinatarul \""
         << destinatar << "\" a fost sters.\n";
    }

    void setExpeditor(string exped) { expeditor = exped; }
    void setDestinatar(string dest) { destinatar = dest; }
    void setGreutate(float gr) { greutate = gr; }
    void setAdresa(string adr) { adresa = adr; }

    void livreaza(string data) {
    if (status == "Livrat") {
        cout << "Coletul este deja livrat!\n";
    } else {
        status = "Livrat";
        dataLivrare = data;
    }
}

    void afiseaza() {
        cout << "\n========= COLET =========\n";
        cout << "Expeditor   : " << expeditor << endl;
        cout << "Destinatar  : " << destinatar << endl;
        cout << "Greutate    : " << greutate << " kg\n";
        cout << "Adresa      : " << adresa << endl;
        cout << "Status      : " << status << endl;
        cout << "Data livrare: " << dataLivrare << endl;
        cout << "========================\n";
    }
};

int main() {
    cout << "=== GESTIUNEA UNUI COLET ===\n\n";
    cout << "CREARE COLET INITIAL\n";

    Colet c1("Mihai Eminescu", "Ion Creanga", 3.2, "Str. Independentei");
    c1.afiseaza();

    cout << "\nCOPIERE COLET\n";
    Colet c2(c1);
    c2.afiseaza();

    cout << "\nMODIFICARE COLET COPIAT\n";
    c2.setDestinatar("Grigore Vieru");
    c2.setGreutate(5.4);
    c2.setAdresa("Str. Stefan cel Mare 15");
    c2.livreaza("18.01.1880");
    c2.afiseaza();
    
    cout << "\nSfarsit program.\n";
    return 0;
}
