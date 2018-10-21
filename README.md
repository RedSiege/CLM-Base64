# CLM-Base64
This project provides Base64 encoding and decoding functionality to PowerShell within Constrained Language Mode. Since this is constrained language mode compliant, it will also run in Full Language Mode.

One option users have is to provide an alternate alpahbet to use for Base64 encoding/decoding. This will allow the user to use a non-standard alphabet. The user-provided alphabet is validated prior to using it.

...probably useful

## ConvertTo-Base64

The ConvertTo-Base64 cmdlet will take a string, or a file, and base64 encode the provided data. If the -OutFile parameter is provided, then the results are saved to the provided file path. Otherwise, the results are displayed to the console.

`ConvertTo-Base64 -String "FortyNorth Security"
ConvertTo-Base64 -FilePath C:\temp\pic.jpg -OutFile C:\temp\encodedpic.txt`

## ConvertFrom-Base64

The ConvertFrom-Base64 cmdlet will take a string, or a file, and base64 decode the provided data. If the -OutFile parameter is provided, then the results are saved to the provided file path. Otherwise, the results are displayed to the console.

`ConvertFrom-Base64 -String "Rm9ydHlOb3J0aCBTZWN1cml0eQ=="
ConvertFrom-Base64 -FilePath C:\temp\encodedpic.txt -OutFile C:\temp\pic.jpg`

## Test-EncodingBase64

This function runs multiple tests to validate that the base64 decoding and encoding functions are properly working by testing the cmdlet results with known good base64 decoding and encoding functions.