---
layout: home
permalink: /
show_language_chooser: false
---

<meta http-equiv="refresh" content="10; URL=/en/">
<p>
  Space After Borders is available in <a href="/it/">Italian</a> and <a href="/en/">English</a>.
</p>
<p>
  You will be redirected to your preferred language or the English page.
</p>

<script>
let supportedLanguages = ["en", "it"];
let browserLanguages = new Set(navigator.languages.map((lang) => lang.split("-").shift().toLowerCase()));
let chosenLanguage;
browserLanguages.forEach((userLanguage) => {
  if (chosenLanguage) {
    // The first chosen language is the best match
    return;
  }
  if (supportedLanguages.includes(userLanguage)) {
    chosenLanguage = userLanguage;
  }
})
if (chosenLanguage === undefined) {
  chosenLanguage = "en"; // default language
}
window.location.href = `/${chosenLanguage}`;
</script>