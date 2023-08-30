#### ALGORITMA TECHNICAL TEST

- Terdapat string "NEGIE1", silahkan reverse alphabet nya dengan angka tetap diakhir kata Hasil = "EIGEN1"
```javascript
const isString = "NEGIE1";
function reverseStr(str) {
  let value = "";
  const splitChar1 = str.slice(5); // 1
  const splitChartStr = str.slice(0, 5); // NEGIE
  const reverse = splitChartStr.split("").reverse().join("");

  const res = (value = reverse.concat(splitChar1));
  return res;
}
console.log("1. ", reverseStr(isString));
```


- Diberikan contoh sebuah kalimat, silahkan cari kata terpanjang dari kalimat tersebut, jika ada kata dengan panjang yang sama silahkan ambil salah satu

	```javascript
	const sentence = "Saya sangat senang mengerjakan soal algoritma";
	const longest = (str) => {
	  let largest = "";
	  str = str.match(/[a-zA-Z0-9]+/gi);
	  for (let i = 0; i < str.length; i++) {
		if (str[i].length > largest.length) {
		  largest = str[i];
		}
	  }
	  return largest;
	};

	console.log(
	  "2. ",
	  `${longest(sentence)} : ${longest(sentence).length} Character`
	);
	```


- Terdapat dua buah array yaitu array INPUT dan array QUERY, silahkan tentukan berapa kali kata dalam QUERY terdapat pada array INPUT

	```javascript
	INPUT = ["xc", "dz", "bbb", "dz"];
	QUERY = ["bbb", "ac", "dz"];
	function inputArr(arr1, arr2) {
	  const value = arr1.filter((e) => arr2.indexOf(e) !== -1);
	  const res = value.map((i, e) => {
		return {
		  label: e,
		  value: e === 0 ? (i = "xc") : i,
		};
	  });

	  return res;
	}
	console.log("3.  OUTPUT :", inputArr(INPUT, QUERY));
	```


- Silahkan cari hasil dari pengurangan dari jumlah diagonal sebuah matrik NxN Contoh

	```javascript
	function diagonalDifference(matrix) {
	  let diagonal1 = 0;
	  let diagonal2 = 0;

	  for (let i = 0; i < matrix.length; i++) {
		// Menghitung jumlah diagonal utama
		diagonal1 += matrix[i][i];

		// Menghitung jumlah diagonal kedua
		diagonal2 += matrix[i][matrix.length - i - 1];
	  }

	  // Menghitung hasil pengurangan
	  const result = Math.abs(diagonal1 - diagonal2);
	  return result;
	}

	// Contoh matriks 3x3
	const matrix = [
	  [1, 2, 3],
	  [4, 5, 6],
	  [7, 8, 9],
	];

	const hasil = diagonalDifference(matrix);
	console.log(
	  "4.  Hasil pengurangan antara jumlah diagonal utama dan jumlah diagonal kedua: " +
		hasil
	);
	```
