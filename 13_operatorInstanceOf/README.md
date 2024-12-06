# Operator instanceof
* Kadang ada kasus kita ingin mengecek apakah sebuah object merupakan instance dari class tertentu atau bukan.
* Kita tidak bisa menggunakan operator ``` typeof ```, karena object dari class, jika kita gunakan operator ``` typeof ```, hasilnya adalah "object".
* Operator ``` instanceof ``` akan menghasilkan boolean, true jika benar object tersebut adalah instance object nya, atau false jika bukan.
* Kode: Masalah dengan typeof
  ```TSX
  class Employee {}

  class Manager {}

  const budi = new Employee();
  const sandy = new Manager();

  console.info(typeof budi);
  console.info(typeof sandy);
  ```
* Kode: Operator instanceof
  ```TSX
  class Employee {}

  class Manager {}

  const budi = new Employee();
  const sandy = new Manager();

  expect(budi instanceof Employee).toBe(true);
  expect(budi instanceof Manager).toBe(false);

  expect(sandy instanceof Employee).toBe(false);
  expect(sandy instanceof Manager).toBe(true);
  ```