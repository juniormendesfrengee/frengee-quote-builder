# Frengee Quote Builder

A password-protected page for pricing a Frengee proposal live with a customer. It is served at https://quote.frengee.com through GitHub Pages.

- Fill in the form on the left, and the Investment page on the right updates as you type.
- **Customer view** hides the form so you can share your screen.
- **Copy for proposal** copies the answers file that the `frengee-proposal` Claude skill uses to build the full PDF.

## Password

`index.html` holds only an unlock form and the quote builder encrypted with AES-256-GCM, using a key derived from the team password (PBKDF2-SHA256, 600,000 rounds). The pricing can't be read from this repository or the live site without the password.

To lock this browser again, visit `https://quote.frengee.com/#lock`.

## Updating

The readable page and the lock script are kept outside this repository. To change prices or the password, rebuild with `lock.sh`, then commit and push the new `index.html`.
