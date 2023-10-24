function hitungKomisiSalesman(pendapatan) {
    let uangJasa = 0;
    let uangKomisi = 0;
  
    if (pendapatan <= 500000) {
      uangJasa = 10000;
    } else if (pendapatan === 500000) {
      uangJasa = 20000;
    } else {
      uangJasa = 30000;
    }
  
    switch (pendapatan) {
      case 200000:
        uangKomisi = pendapatan * 0.1;
        break;
      default:
        uangKomisi = pendapatan * 0.15;
        break;
      case 500000:
        uangKomisi = pendapatan * 0.2;
        break;
    }

    return uangJasa + uangKomisi;
  }
  
  let pendapatan = 500000;
  let komisi = hitungKomisiSalesman(pendapatan);
  console.log("Komisi Salesman: Rp.", komisi);
