# coolname-generator-action



Generates coolnames like 'crazy-red-baboon' for use in tagging things with Github Actions

[unique-names-generator](https://github.com/andreasonny83/unique-names-generator) is used to generate the names.

NOTE: UPDATED TO AVOID ENV VARS.

## Parameters

### Inputs

| Parameter   | Default     | Description                             |
| ----------- | ----------- | --------------------------------------- |
| `separator` | `-`         | What separator to use.                  |
| `length`    | `2`         | How many words in the name, `2` or `3`. |
| `style`     | `lowerCase` | Name output case style.                 |

### Outputs

| Parameter | Description               |
| --------- | ------------------------- |
| `name`    | The generated random name |

## Example usage

```yml
uses: thclark/coolname-generator-action@0.0.1
```

```yml
uses: thclark/coolname-generator-action@0.0.1
id: generator
with:
  separator: "_"
  length: "4"
  style: "upperCase"

name: test generator output
run: echo "latest,${{ steps.generator.outputs.name }}"
```

## Development

See the [build instructions](https://docs.github.com/en/actions/creating-actions/creating-a-javascript-action#commit-tag-and-push-your-action-to-github)
for node based actions in order to build `index.js` to `dist/index.js`
