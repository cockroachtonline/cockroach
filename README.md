// โค้ดเดิม (ใช้ไม่ได้บน GitHub)
// google.script.run.withSuccessHandler(...).registerUser(alias);

// โค้ดใหม่ (ใช้ได้ทั่วโลก)
fetch("URL_WEB_APP_ของ_GAS", {
  method: "POST",
  body: JSON.stringify({ action: "register", alias: alias }),
  mode: "no-cors" // สำคัญมากเพื่อป้องกันบั๊กความปลอดภัยเบราว์เซอร์
}).then(() => {
  switchToMain(alias);
});
