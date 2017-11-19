# QQ Numbas

The `qqnumbas` package defines a macro to generate a [Numbas][numbas] exam as a byproduct
when typesetting multiple choice questions.

[numbas]: https://www.numbas.org.uk

## Usage

The package provides the command `\quickquestion{...}` that takes parameters in pgfkeys style:

```latex
\quickquestion{%
	name = {Question Name},
	prompt = {
		Here goes the question prompt. Multiple paragraphs are not allowed (yet).
	},
	choices={
		{Option A. Can be pure text.},
		{Option B. Can have inline math $e^{i\pi}=-1$},
		{Option C. Can have blockmath $$},
		{Option D. Paragraphs aren't allowed here either.} % Without trailing comma
	},
	answer={b}, % Single lowercase letter. Can be any of: abcd
}
```


## Authors

- [ManuelBlanc](https://github.com/ManuelBlanc)

## Acknowledgements

Thanks to the [TeX StackExchange][texse] for all the helpful content.
Special thanks to egreg for [answering my question][question] about how to protect the backslashes in the output.


[texse]: https://tex.stackexchange.com
[question]: https://tex.stackexchange.com/a/402045/90126
