# Maximum Bot Translations

The text Maximum Bot uses in Discord and on its dashboard, in every language it speaks. Help us check the translations we have, or add a new language.

## Languages

| Language | File | Status |
|---|---|---|
| 🇬🇧 English | [`ENGL.json`](ENGL.json) | Original text. All other languages are translated from this file. |
| 🇫🇷 French | [`FREN.json`](FREN.json) | Complete. Reviewers welcome. |
| 🇪🇸 Spanish | [`SPAN.json`](SPAN.json) | Complete, **needs review** by a native speaker before it goes live |
| 🇹🇷 Turkish | [`TURK.json`](TURK.json) | Complete, **needs review** by a native speaker before it goes live |
| ➕ New language | [`TEMPLATE.json`](TEMPLATE.json) | Blank file to start a new translation |

Every file has the same 1,831 lines in the same order.

## How the files work

Each file is grouped into sections. Each line has a **key** on the left, which you never change, and the **text** on the right, which you translate:

```json
"purge": {
  "title": "🧹 Messages Purged",
  "done_one": "✅ Deleted {count} message.",
  "done_other": "✅ Deleted {count} messages."
}
```

Most sections are named after a bot command (`purge` is `/purge`, `help` is `/help`). Two are different:

- **`slash`** is the command descriptions people see in Discord's `/` menu.
- **`dash`** is the web dashboard.

## Rules

1. **Only change the text on the right of the `:`.** Never rename, add or remove keys.
2. **Keep everything in `{curly braces}` exactly as it is**, such as `{user}`, `{count}` or `{channel}`. The bot replaces these with real values. You can move them anywhere in the sentence, but don't translate or remove them.
3. **Plurals:** keys ending in `_one` are the singular and `_other` the plural. If your language uses the same word for both, write the same text twice.
4. **Lines under `slash` must be 100 characters or fewer.** That's Discord's limit.
5. **Keep Discord formatting:** `**bold**`, `` `code` ``, links and emojis stay where they make sense.
6. **Write the way people talk on Discord.** Use a friendly, natural tone, not a word-for-word translation.
7. **Keep it valid JSON:** a straight `"` inside your text must be written as `\"`, and keep the commas between lines.

## Reviewing a translation

1. Open [`ENGL.json`](ENGL.json) and the language file side by side. The lines match up one to one.
2. Look for anything that's wrong, sounds unnatural, or isn't what a Discord user would say.
3. Send us your fixes. Name the key and give your better wording. For example:

   > `purge.title`: "🧹 Messages supprimés" should be "🧹 Messages effacés"

## Adding a new language

1. Download [`TEMPLATE.json`](TEMPLATE.json) and rename it with a four-letter code, for example `GERM.json` for German or `ITAL.json` for Italian.
2. Fill in every `""` using [`ENGL.json`](ENGL.json) as your guide.
3. Send us the finished file. Partial files are welcome too. Any line left blank shows in English.

## Sending your work

- **On GitHub:** fork this repository, edit the file, and open a pull request. For a review, you can also open an issue listing your fixes.
- **No GitHub account?** Post your fixes or your file in our Discord server, or reach us at [support.maximumstudios.xyz](https://support.maximumstudios.xyz).

Every submission is checked automatically for missing lines, broken placeholders and text that's too long before it goes into the bot. You don't need to be perfect. We'll catch the technical problems.

## Credits

Everyone who translates or reviews a language will be credited. Tell us the name you'd like to be listed under.

---

By contributing, you agree that your translations can be used in Maximum Bot. [Terms of Service](https://tos.maximumstudios.xyz) · [Privacy Policy](https://privacy.maximumstudios.xyz)
