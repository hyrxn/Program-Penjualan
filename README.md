#include<stdio.h>
#include<string.h>

struct Inventory {
 char namaItem[100];
 int qtyItem;
 long long int hargaJual;
};

void tambahBarang() {
 struct Inventory brg;
 scanf("%s", brg.namaItem);
 scanf("%d", &brg.qtyItem);
 scanf("%lld", &brg.hargaJual);
 FILE *fp = fopen("inventory.txt", "a");
 fprintf(fp, "%s#%d#%lld\n", brg.namaItem, brg.qtyItem, brg.hargaJual);
 fclose(fp);
}
int main() {
 int choice;
 do{
  printf("1. Nama Barang\n");
  printf("2. Tambah Barang\n");
  printf("3. Update Harga\n");
  printf("4. Lihat Semua Daftar\n");
  printf("5. Exit\n");
  scanf("%d\n", &choice);
  switch(choice) {
   case 1: {
    break;
   }
   case 2: {
    tambahBarang();
    break;
   }
   case 3: {
    break;
   }
   case 4: {
    break;
   }
   case 5: {
    break;
   }
  }
 } while(choice != 5);
 return 0;
}
