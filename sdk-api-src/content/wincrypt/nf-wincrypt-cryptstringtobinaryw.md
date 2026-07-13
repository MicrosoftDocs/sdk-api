---
UID: NF:wincrypt.CryptStringToBinaryW
title: CryptStringToBinaryW function (wincrypt.h)
description: Converts a formatted string into an array of bytes. (Unicode)
helpviewer_keywords: ["CRYPT_STRING_ANY", "CRYPT_STRING_BASE64", "CRYPT_STRING_BASE64HEADER", "CRYPT_STRING_BASE64REQUESTHEADER", "CRYPT_STRING_BASE64X509CRLHEADER", "CRYPT_STRING_BASE64_ANY", "CRYPT_STRING_BINARY", "CRYPT_STRING_HEX", "CRYPT_STRING_HEXADDR", "CRYPT_STRING_HEXASCII", "CRYPT_STRING_HEXASCIIADDR", "CRYPT_STRING_HEXRAW", "CRYPT_STRING_HEX_ANY", "CRYPT_STRING_STRICT", "CryptStringToBinary", "CryptStringToBinary function [Security]", "CryptStringToBinaryW", "_crypto2_cryptstringtobinary", "security.cryptstringtobinary", "wincrypt/CryptStringToBinary", "wincrypt/CryptStringToBinaryW"]
old-location: security\cryptstringtobinary.htm
tech.root: security
ms.assetid: 13b6f5ef-174a-4254-8492-6e7dcc58945f
ms.date: 12/05/2018
ms.keywords: CRYPT_STRING_ANY, CRYPT_STRING_BASE64, CRYPT_STRING_BASE64HEADER, CRYPT_STRING_BASE64REQUESTHEADER, CRYPT_STRING_BASE64X509CRLHEADER, CRYPT_STRING_BASE64_ANY, CRYPT_STRING_BINARY, CRYPT_STRING_HEX, CRYPT_STRING_HEXADDR, CRYPT_STRING_HEXASCII, CRYPT_STRING_HEXASCIIADDR, CRYPT_STRING_HEXRAW, CRYPT_STRING_HEX_ANY, CRYPT_STRING_STRICT, CryptStringToBinary, CryptStringToBinary function [Security], CryptStringToBinaryA, CryptStringToBinaryW, _crypto2_cryptstringtobinary, security.cryptstringtobinary, wincrypt/CryptStringToBinary, wincrypt/CryptStringToBinaryA, wincrypt/CryptStringToBinaryW
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CryptStringToBinaryW (Unicode) and CryptStringToBinaryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptStringToBinaryW
 - wincrypt/CryptStringToBinaryW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CryptStringToBinary
 - CryptStringToBinaryA
 - CryptStringToBinaryW
---

# CryptStringToBinaryW function


## -description

The <b>CryptStringToBinary</b> function converts a formatted string into an array of bytes.

## -parameters

### -param pszString [in]

A pointer to a string that contains the formatted string to be converted.

### -param cchString [in]

The number of characters of the formatted string to be converted, not including the terminating <b>NULL</b> character. If this parameter is zero,  <i>pszString</i> is considered to be a null-terminated string.

### -param dwFlags [in]

Indicates the format of the string to be converted. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_BASE64HEADER"></a><a id="crypt_string_base64header"></a><dl>
<dt><b>CRYPT_STRING_BASE64HEADER</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Base64 between lines of the form `-----BEGIN ...-----` and `-----END ...-----`.
See Remarks below.
</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_BASE64"></a><a id="crypt_string_base64"></a><dl>
<dt><b>CRYPT_STRING_BASE64</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Base64, without headers.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_BINARY"></a><a id="crypt_string_binary"></a><dl>
<dt><b>CRYPT_STRING_BINARY</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Pure binary copy.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_BASE64REQUESTHEADER"></a><a id="crypt_string_base64requestheader"></a><dl>
<dt><b>CRYPT_STRING_BASE64REQUESTHEADER</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Base64 between lines of the form `-----BEGIN ...-----` and `-----END ...-----`.
See Remarks below.
</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_HEX"></a><a id="crypt_string_hex"></a><dl>
<dt><b>CRYPT_STRING_HEX</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Hexadecimal only format.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_HEXASCII"></a><a id="crypt_string_hexascii"></a><dl>
<dt><b>CRYPT_STRING_HEXASCII</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
Hexadecimal format with <a href="/windows/desktop/SecGloss/a-gly">ASCII</a> character display.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_BASE64_ANY"></a><a id="crypt_string_base64_any"></a><dl>
<dt><b>CRYPT_STRING_BASE64_ANY</b></dt>
<dt>0x00000006</dt>
</dl>
</td>
<td width="60%">
Tries the following, in order: 




<dl>
<dd>CRYPT_STRING_BASE64HEADER</dd>
<dd>CRYPT_STRING_BASE64</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_ANY"></a><a id="crypt_string_any"></a><dl>
<dt><b>CRYPT_STRING_ANY</b></dt>
<dt>0x00000007</dt>
</dl>
</td>
<td width="60%">
Tries the following, in order: 




<dl>
<dd>CRYPT_STRING_BASE64HEADER</dd>
<dd>CRYPT_STRING_BASE64</dd>
<dd>CRYPT_STRING_BINARY</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_HEX_ANY"></a><a id="crypt_string_hex_any"></a><dl>
<dt><b>CRYPT_STRING_HEX_ANY</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Tries the following, in order: 




<dl>
<dd>CRYPT_STRING_HEXADDR</dd>
<dd>CRYPT_STRING_HEXASCIIADDR</dd>
<dd>CRYPT_STRING_HEX</dd>
<dd>CRYPT_STRING_HEXRAW</dd>
<dd>CRYPT_STRING_HEXASCII</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_BASE64X509CRLHEADER"></a><a id="crypt_string_base64x509crlheader"></a><dl>
<dt><b>CRYPT_STRING_BASE64X509CRLHEADER</b></dt>
<dt>0x00000009</dt>
</dl>
</td>
<td width="60%">
Base64 between lines of the form `-----BEGIN ...-----` and `-----END ...-----`.
See Remarks below.
</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_HEXADDR"></a><a id="crypt_string_hexaddr"></a><dl>
<dt><b>CRYPT_STRING_HEXADDR</b></dt>
<dt>0x0000000a</dt>
</dl>
</td>
<td width="60%">
Hex, with address display.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_HEXASCIIADDR"></a><a id="crypt_string_hexasciiaddr"></a><dl>
<dt><b>CRYPT_STRING_HEXASCIIADDR</b></dt>
<dt>0x0000000b</dt>
</dl>
</td>
<td width="60%">
Hex, with ASCII character and address display.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_HEXRAW"></a><a id="crypt_string_hexraw"></a><dl>
<dt><b>CRYPT_STRING_HEXRAW</b></dt>
<dt>0x0000000c</dt>
</dl>
</td>
<td width="60%">
A raw hexadecimal string.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_STRICT"></a><a id="crypt_string_strict"></a><dl>
<dt><b>CRYPT_STRING_STRICT</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Set this flag for Base64 data to specify that the end of the binary data contain only white space and at most three equals "=" signs.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
</table>

### -param pbBinary [in]

A pointer to a buffer that receives the returned sequence of bytes. If this parameter is <b>NULL</b>, the function calculates the length of the buffer needed and returns the size, in bytes, of required memory in the <b>DWORD</b> pointed to by <i>pcbBinary</i>.

### -param pcbBinary [in, out]

A pointer to a <b>DWORD</b> variable that, on entry, contains the size, in bytes, of the <i>pbBinary</i> buffer. After the function returns, this variable contains the number of bytes copied to the buffer. If this value is not large enough to contain all of the data, the function fails and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_MORE_DATA</b>.

If <i>pbBinary</i> is <b>NULL</b>, the <b>DWORD</b> pointed to by <i>pcbBinary</i> is ignored.

### -param pdwSkip [out]

A pointer to a <b>DWORD</b> value that receives the number of characters skipped to reach the beginning of the
`-----BEGIN ...-----` header.
If no header is present, then the <b>DWORD</b> is set to zero.
This parameter is optional and can be <b>NULL</b> if it is not needed.

### -param pdwFlags [out]

A pointer to a <b>DWORD</b> value that receives the flags actually used in the conversion. These are the same flags used for the <i>dwFlags</i> parameter. In many cases, these will be the same flags that were passed in the <i>dwFlags</i> parameter. If <i>dwFlags</i> contains one of the following flags, this value will receive a flag that indicates the actual format of the string. This parameter is optional and can be <b>NULL</b> if it is not needed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_ANY"></a><a id="crypt_string_any"></a><dl>
<dt><b>CRYPT_STRING_ANY</b></dt>
</dl>
</td>
<td width="60%">
This variable will receive one of the following values. Each value indicates the actual format of the string.

<dl>
<dd>CRYPT_STRING_BASE64HEADER</dd>
<dd>CRYPT_STRING_BASE64</dd>
<dd>CRYPT_STRING_BINARY</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_BASE64_ANY"></a><a id="crypt_string_base64_any"></a><dl>
<dt><b>CRYPT_STRING_BASE64_ANY</b></dt>
</dl>
</td>
<td width="60%">
This variable will receive one of the following values. Each value indicates the actual format of the string.

<dl>
<dd>CRYPT_STRING_BASE64HEADER</dd>
<dd>CRYPT_STRING_BASE64</dd>
</dl>
</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_HEX_ANY"></a><a id="crypt_string_hex_any"></a><dl>
<dt><b>CRYPT_STRING_HEX_ANY</b></dt>
</dl>
</td>
<td width="60%">
This variable will receive one of the following values. Each value indicates the actual format of the string.

<dl>
<dd>CRYPT_STRING_HEXADDR</dd>
<dd>CRYPT_STRING_HEXASCIIADDR</dd>
<dd>CRYPT_STRING_HEX</dd>
<dd>CRYPT_STRING_HEXRAW</dd>
<dd>CRYPT_STRING_HEXASCII</dd>
</dl>
</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>).

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptbinarytostringa">CryptBinaryToString</a>

## -remarks

The
<b>CRYPT_STRING_BASE64HEADER</b>,
<b>CRYPT_STRING_BASE64REQUESTHEADER</b>,
and
<b>CRYPT_STRING_BASE64X509CRLHEADER</b>
flags are all treated identically by this function:
They attempt to parse the first block of
base64-encoded data between lines of the form
`-----BEGIN ...-----` and `-----END ...-----`.
The `...` portions are ignored, and they need not match.
If parsing is successful, the value passed in the <i>dwFlags</i> parameter
is returned in the <b>DWORD</b> pointed to by the <i>pdwFlags</i> parameter.
Note that a value of
<b>CRYPT_STRING_BASE64REQUESTHEADER</b>
or
<b>CRYPT_STRING_BASE64X509CRLHEADER</b>
does not mean that a request header or
<a href="/windows/desktop/SecGloss/c-gly#_SECURITY_X.509_GLY">X.509</a>
<a href="/windows/desktop/SecGloss/c-gly#_security_certificate_revocation_list_gly">certificate revocation list</a> (CRL)
was found.

> [!NOTE]
> The wincrypt.h header defines CryptStringToBinary as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
