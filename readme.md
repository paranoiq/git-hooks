
**pre-commit**

kontroluje:

PHP:
- syntaktická správnost PHP (lint), *zatím nepoužívá parallel lint*
- kontrola coding standards, pokud je přítomné phpcs v adresáři bin

JS:
- syntaktická správnost a CS JavaScriptu (JSHint)

Migrace:
- chybějící jména cizích klíčů (nelze je pak mazat/upravovat)
- u sloupců nesmí být uvedeno collation (má se brát výchozí z databáze)
- u pohledů nesmí být definer (uživatel nemusí na cílovém stroji existovat)
- práva pohledů musí být podle uživatele, nikoli definera (větší bezpečnost; definer nemusí existovat)
- nelze založit tabulku `log` (MySQL bug)

**post-checkout**

spustí `phing` pro build projektu
