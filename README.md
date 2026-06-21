# isi-kuesioner-siam

1. Buka halaman kuesioner SIAM
2. Tekan F12 dan masuk ke tab console
3. Paste code di bawah ini
```js
(() => {
  document.querySelectorAll('input[type="radio"][value="5"]')
    .forEach(el => {
      el.checked = true;
      el.dispatchEvent(new Event("change", { bubbles: true }));
    });

  document.querySelectorAll('textarea').forEach(el => {
    if (!el.value.trim()) {
      el.value = "isi komentar";
      el.dispatchEvent(new Event("input", { bubbles: true }));
    }
  });

  console.log("Done. Cek lagi sebelum submit.");
})();
```

4. Sesuaikan nilai `value=x` dari 1-5
