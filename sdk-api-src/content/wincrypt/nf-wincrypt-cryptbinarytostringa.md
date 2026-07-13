---
UID: NF:wincrypt.CryptBinaryToStringA
title: CryptBinaryToStringA function (wincrypt.h)
description: Converts an array of bytes into a formatted string. (ANSI)
helpviewer_keywords: ["CRYPT_STRING_BASE64", "CRYPT_STRING_BASE64HEADER", "CRYPT_STRING_BASE64REQUESTHEADER", "CRYPT_STRING_BASE64X509CRLHEADER", "CRYPT_STRING_BINARY", "CRYPT_STRING_HEX", "CRYPT_STRING_HEXADDR", "CRYPT_STRING_HEXASCII", "CRYPT_STRING_HEXASCIIADDR", "CRYPT_STRING_HEXRAW", "CRYPT_STRING_NOCR", "CRYPT_STRING_NOCRLF", "CRYPT_STRING_STRICT", "CryptBinaryToStringA", "wincrypt/CryptBinaryToStringA"]
old-location: security\cryptbinarytostring.htm
tech.root: security
ms.assetid: e6bdf931-fba3-4a33-b22e-5f818f565842
ms.date: 12/05/2018
ms.keywords: CRYPT_STRING_BASE64, CRYPT_STRING_BASE64HEADER, CRYPT_STRING_BASE64REQUESTHEADER, CRYPT_STRING_BASE64X509CRLHEADER, CRYPT_STRING_BINARY, CRYPT_STRING_HEX, CRYPT_STRING_HEXADDR, CRYPT_STRING_HEXASCII, CRYPT_STRING_HEXASCIIADDR, CRYPT_STRING_HEXRAW, CRYPT_STRING_NOCR, CRYPT_STRING_NOCRLF, CRYPT_STRING_STRICT, CryptBinaryToString, CryptBinaryToString function [Security], CryptBinaryToStringA, CryptBinaryToStringW, _crypto2_cryptbinarytostring, security.cryptbinarytostring, wincrypt/CryptBinaryToString, wincrypt/CryptBinaryToStringA, wincrypt/CryptBinaryToStringW
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CryptBinaryToStringW (Unicode) and CryptBinaryToStringA (ANSI)
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
 - CryptBinaryToStringA
 - wincrypt/CryptBinaryToStringA
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
 - CryptBinaryToString
 - CryptBinaryToStringA
 - CryptBinaryToStringW
---

# CryptBinaryToStringA function


## -description

The <b>CryptBinaryToString</b> function converts an array of bytes into a formatted string.

## -parameters

### -param pbBinary [in]

A pointer to the array of bytes to be converted into a string.

### -param cbBinary [in]

The number of elements in the <i>pbBinary</i> array.

### -param dwFlags [in]

Specifies the format of the resulting formatted string. This parameter can be one of the following values.

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
Base64, with certificate beginning and ending headers.

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
Base64, with request beginning and ending headers.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_HEX"></a><a id="crypt_string_hex"></a><dl>
<dt><b>CRYPT_STRING_HEX</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Hexadecimal only.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_HEXASCII"></a><a id="crypt_string_hexascii"></a><dl>
<dt><b>CRYPT_STRING_HEXASCII</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
Hexadecimal, with <a href="/windows/desktop/SecGloss/a-gly">ASCII</a> character display.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_BASE64X509CRLHEADER"></a><a id="crypt_string_base64x509crlheader"></a><dl>
<dt><b>CRYPT_STRING_BASE64X509CRLHEADER</b></dt>
<dt>0x00000009</dt>
</dl>
</td>
<td width="60%">
Base64, with <a href="/windows/desktop/SecGloss/x-gly">X.509</a> CRL beginning and ending headers.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_HEXADDR"></a><a id="crypt_string_hexaddr"></a><dl>
<dt><b>CRYPT_STRING_HEXADDR</b></dt>
<dt>0x0000000a</dt>
</dl>
</td>
<td width="60%">
Hexadecimal, with address display.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_HEXASCIIADDR"></a><a id="crypt_string_hexasciiaddr"></a><dl>
<dt><b>CRYPT_STRING_HEXASCIIADDR</b></dt>
<dt>0x0000000b</dt>
</dl>
</td>
<td width="60%">
Hexadecimal, with ASCII character and address display.

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
<td width="40%"><a id="CRYPT_STRING_BASE64URI"></a><a id="crypt_string_base64uri"></a><dl>
<dt><b>CRYPT_STRING_BASE64URI</b></dt>
<dt>0x0000000d</dt>
</dl>
</td>
<td width="60%">
Base64, without headers, with "+" replaced by "-" and "/" replaced by "_" as defined in RFC 4648 Section 5.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_STRICT"></a><a id="crypt_string_strict"></a><dl>
<dt><b>CRYPT_STRING_STRICT</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Enforce strict decoding of ASN.1 text formats.  Some ASN.1 binary BLOBS can have the first few bytes of the BLOB incorrectly interpreted as Base64 text. In this case, the rest of the text is ignored. Use this flag to enforce complete decoding of the BLOB.


<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.



</td>
</tr>
</table>
 


In addition to the values above, one or more of the following values can be specified to modify the behavior of the function.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_NOCRLF"></a><a id="crypt_string_nocrlf"></a><dl>
<dt><b>CRYPT_STRING_NOCRLF</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
Do not append any new line characters to the encoded string. The default behavior is to use a carriage return/line feed (CR/LF) pair (0x0D/0x0A) to represent a new line.


<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.



</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STRING_NOCR"></a><a id="crypt_string_nocr"></a><dl>
<dt><b>CRYPT_STRING_NOCR</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
Only use the line feed (LF) character (0x0A) for a new line. The default behavior is to use a CR/LF pair (0x0D/0x0A) to represent a new line.

</td>
</tr>
</table>

### -param pszString [out, optional]

A pointer to a buffer that receives the converted string. To calculate the number of characters that must be allocated to hold the returned string, set this parameter to <b>NULL</b>. The function will place the required number of characters, including the terminating <b>NULL</b> character, in the value pointed to by <i>pcchString</i>.

### -param pcchString [in, out]

A pointer to a <b>DWORD</b> variable that contains the size, in <b>TCHAR</b>s, of the <i>pszString</i> buffer. If <i>pszString</i> is <b>NULL</b>, the function calculates the length of the return string (including the terminating null character) in <b>TCHAR</b>s and returns it in this parameter. If <i>pszString</i> is not <b>NULL</b> and big enough, the function converts the binary data into a specified string format including the terminating null character, but <i>pcchString</i> receives the length in <b>TCHAR</b>s, not including the terminating null character.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>).

## -remarks

With the exception of when <b>CRYPT_STRING_BINARY</b> encoding is used, all strings are appended with a new line sequence. By default, the new line sequence is a CR/LF pair (0x0D/0x0A). If the <i>dwFlags</i> parameter contains the <b>CRYPT_STRING_NOCR</b> flag, then the new line sequence is a LF character (0x0A). If the <i>dwFlags</i> parameter contains the <b>CRYPT_STRING_NOCRLF</b> flag, then no new line sequence is appended to the string.





> [!NOTE]
> The wincrypt.h header defines CryptBinaryToString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptstringtobinarya">CryptStringToBinary</a>
