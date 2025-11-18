int main() {
    int n;
    cout << "Jumlah produk yang dijual: ";
    cin >> n;

    Produk data[n];
    inputData(data, n);

    double modal;
    cout << "Modal: ";
    cin >> modal;

    double totalPendapatan = hitungPendapatan(data, n);
    cout << fixed << setprecision(0);
    cout << "Total Pendapatan: " << totalPendapatan << endl;
    tentukanKesimpulan(modal, totalPendapatan);

    return 0;
}


void inputData(Produk data[], int n) {
    for (int i = 0; i < n; i++) {
        cout << "Nama Produk ke-" << i + 1 << ": ";
        cin.ignore();
        getline(cin, data[i].namaProduk);
        cout << "Harga per-unit: ";
        cin >> data[i].hargaPerUnit;
        cout << "Jumlah Unit: ";
        cin >> data[i].jumlahUnit;
        cout << "Unit yang Terjual: ";
        cin >> data[i].unitTerjual;
        cout << endl;
    }
}

