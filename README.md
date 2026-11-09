# 🐾 can-dogs-eat

A small, open list of everyday human foods and whether a dog can have them, as plain JSON.

Every food gets one of three verdicts:

| verdict | meaning |
|---|---|
| `ok` | fine in small, plain amounts (no butter, salt, onion, garlic or seasoning) |
| `careful` | depends on amount, preparation, or the dog |
| `no` | toxic or dangerous: keep it away |

...plus a one-line reason in plain words, an emoji, and tags like `thanksgiving`, `christmas`, `halloween`, `summer` so you can pull out a holiday list.

I'm Charlie, a mini goldendoodle who has asked "can I have some?" at every meal of her life. I made this so people building pet apps, bots, recipe sites or holiday checklists don't have to start from scratch.

## Use it

```js
const res = await fetch("https://raw.githubusercontent.com/imcharliethedog/can-dogs-eat/main/foods.json");
const { foods } = await res.json();

const holiday = foods.filter(f => f.tags.includes("christmas"));
const noNo = foods.filter(f => f.verdict === "no").map(f => f.name);
console.log(noNo);
```

Each entry looks like:

```json
{"id": "grapes-raisins", "name": "Grapes, raisins, currants, sultanas", "emoji": "🍇",
 "verdict": "no", "reason": "Can cause kidney failure, even in small amounts.", "tags": ["fruit", "christmas"]}
```

## Try it by tapping

There's a friendly version you can tap through, with a little dot dog who wags or sulks: **[Can I Have Some? (Thanksgiving plate checker)](http://imcharliethedog.com/go/thanksgiving)**.

## Important

**I'm a dog, not a vet.** This is general information, kept deliberately conservative. Dogs differ (size, allergies, health conditions like pancreatitis or kidney disease), so ask your vet about your own dog. If your dog ate something worrying, call your vet or an emergency line right away:

- ASPCA Animal Poison Control (US): **(888) 426-4435**
- Pet Poison Helpline (US/Canada): **(855) 764-7661**

(fees may apply)

## Contributing

Spotted a mistake, or want a food added? Open an issue or PR, ideally with a source from a vet school, the ASPCA, or a similar reputable place. Corrections are very welcome.

## License

CC0 1.0: public domain. Use it for anything.

---
More dotty things from me: [imcharliethedog.com](http://imcharliethedog.com/)
