# BHL-Thesaurus-wrapper
A simple Python wrapper for the [BigHugeLabs Thesaurus](http://words.bighugelabs.com).
The wrapper has been tested in Python 3.5 but not 3.6. Please report any issues.

## Dependencies
Both packages are included in the standard library.

1. json
2. requests

### Thesaurus
The main wrapper object.

`Thesaurus(`*`key, version=2`*`)`

#### Methods:

###### `rawRequest(`*`word, format="json"`*`)`
- returns the request object from the requests

###### `rawText(`*`word, format="json"`*`)`
- returns the raw text of the request

###### `loadedObj(`*`word`*`)`
- returns a Response object with a loaded dict

###### `rawObj(`*`word`*`)`
- returns a loaded dict


### Response
The object responses are stored in.

#### Attributes:

###### data
- the data (type `dict` or `string`) of the response

###### status_code
- the HTTP status code of the response


### Exceptions

###### ErrorCode404
- raised upon a status code of 404

###### ErrorCode500
- raised upon a status code of 500


## Example
```py
import thesaurus

thes = thesaurus.Thesaurus("YOUR KEY")
word_stuff = thes.rawText("stuff")
print(word_stuff)
```
