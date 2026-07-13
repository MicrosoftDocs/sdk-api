---
UID: NF:wincrypt.CryptDecodeObject
title: CryptDecodeObject function (wincrypt.h)
description: The CryptDecodeObject function decodes a structure of the type indicated by the lpszStructType parameter. The use of CryptDecodeObjectEx is recommended as an API that performs the same function with significant performance improvements.
helpviewer_keywords: ["CRYPT_DECODE_NOCOPY_FLAG","CRYPT_DECODE_NO_SIGNATURE_BYTE_REVERSAL_FLAG","CRYPT_DECODE_SHARE_OID_STRING_FLAG","CRYPT_DECODE_TO_BE_SIGNED_FLAG","CRYPT_UNICODE_NAME_DECODE_DISABLE_IE4_UTF8_FLAG","CryptDecodeObject","CryptDecodeObject function [Security]","_crypto2_cryptdecodeobject","security.cryptdecodeobject","wincrypt/CryptDecodeObject"]
old-location: security\cryptdecodeobject.htm
tech.root: security
ms.assetid: 7d5ed4f4-9d76-4a16-9059-27b0edd83459
ms.date: 12/05/2018
ms.keywords: CRYPT_DECODE_NOCOPY_FLAG, CRYPT_DECODE_NO_SIGNATURE_BYTE_REVERSAL_FLAG, CRYPT_DECODE_SHARE_OID_STRING_FLAG, CRYPT_DECODE_TO_BE_SIGNED_FLAG, CRYPT_UNICODE_NAME_DECODE_DISABLE_IE4_UTF8_FLAG, CryptDecodeObject, CryptDecodeObject function [Security], _crypto2_cryptdecodeobject, security.cryptdecodeobject, wincrypt/CryptDecodeObject
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - CryptDecodeObject
 - wincrypt/CryptDecodeObject
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
 - CryptDecodeObject
---

# CryptDecodeObject function


## -description

The <b>CryptDecodeObject</b> function decodes a structure of the type indicated by the <i>lpszStructType</i> parameter. The use of 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobjectex">CryptDecodeObjectEx</a> is recommended as an API that performs the same function with significant performance improvements.

## -parameters

### -param dwCertEncodingType [in]

Type of encoding used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>
<div class="alert"><b>Note</b>  Either a certificate or <a href="/windows/desktop/SecGloss/m-gly">message encoding type</a> is required. X509_ASN_ENCODING is the default. If that type is indicated, it is used. Otherwise, if the PKCS7_ASN_ENCODING type is indicated, it is used.</div>
<div> </div>

### -param lpszStructType [in]

A pointer to an OID defining the structure type. If the high-order word of the <i>lpszStructType</i> parameter is zero, the low-order word specifies the integer identifier for the type of the specified structure. Otherwise, this parameter is a long pointer to a null-terminated string.

For more information about object identifier strings, their predefined constants and corresponding structures, see 
<a href="/windows/desktop/SecCrypto/constants-for-cryptencodeobject-and-cryptdecodeobject">Constants for CryptEncodeObject and CryptDecodeObject</a>.

### -param pbEncoded [in]

A pointer to the encoded structure to be decoded.

### -param cbEncoded [in]

Number of bytes pointed to by <i>pbEncoded</i>.

### -param dwFlags [in]

The following flags are defined. They can be combined with a bitwise-<b>OR</b> operation.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DECODE_NOCOPY_FLAG"></a><a id="crypt_decode_nocopy_flag"></a><dl>
<dt><b>CRYPT_DECODE_NOCOPY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
This flag can be set to indicate that "no copy" optimization is enabled. This optimization, where applicable, updates the <i>pvStructInfo</i> parameter to point to content residing within <i>pbEncoded</i> instead of making a copy of the content and appending it to <i>pvStructInfo</i>. For applicable cases, less memory needs to be allocated by the calling application and execution is faster because a copy is not being made. Note that the trade-off when performing a "no copy" decoding is that <i>pbEncoded</i> cannot be freed until <i>pvStructInfo</i> is freed.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_UNICODE_NAME_DECODE_DISABLE_IE4_UTF8_FLAG"></a><a id="crypt_unicode_name_decode_disable_ie4_utf8_flag"></a><dl>
<dt><b>CRYPT_UNICODE_NAME_DECODE_DISABLE_IE4_UTF8_FLAG</b></dt>
</dl>
</td>
<td width="60%">
This flag is applicable when decoding X509_UNICODE_NAME, X509_UNICODE_NAME_VALUE, or X509_UNICODE_ANY_STRING. By default, CERT_RDN_T61_STRING encoded values are initially decoded as UTF8. If the UTF8 decoding fails, then the value is decoded as eight-bit characters. If this flag is set, it skips the initial attempt to decode the value as UTF8 and decodes the value as eight-bit characters.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DECODE_TO_BE_SIGNED_FLAG"></a><a id="crypt_decode_to_be_signed_flag"></a><dl>
<dt><b>CRYPT_DECODE_TO_BE_SIGNED_FLAG</b></dt>
</dl>
</td>
<td width="60%">
By default, the contents of the buffer pointed to by <i>pbEncoded</i> included the signed content and the signature. If this flag is set, the buffer includes only the "to be signed" content. This flag is applicable to X509_CERT_TO_BE_SIGNED, X509_CERT_CRL_TO_BE_SIGNED, X509_CRT_REQUEST_TO_BE_SIGNED, and X509_KEYGEN_REQUEST_TO_BE_SIGNED objects.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DECODE_SHARE_OID_STRING_FLAG"></a><a id="crypt_decode_share_oid_string_flag"></a><dl>
<dt><b>CRYPT_DECODE_SHARE_OID_STRING_FLAG</b></dt>
</dl>
</td>
<td width="60%">
When this flag is set, the OID strings are allocated in Crypt32.dll and shared instead of being copied into the returned data structure. This flag can be set if Crypt32.dll is not unloaded before the caller is unloaded.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DECODE_NO_SIGNATURE_BYTE_REVERSAL_FLAG"></a><a id="crypt_decode_no_signature_byte_reversal_flag"></a><dl>
<dt><b>CRYPT_DECODE_NO_SIGNATURE_BYTE_REVERSAL_FLAG</b></dt>
</dl>
</td>
<td width="60%">
By default, the signature bytes are reversed. If this flag is set, this byte reversal is inhibited.

</td>
</tr>
</table>

### -param pvStructInfo [out]

A pointer to a buffer to receive the decoded structure. When the buffer that is specified is not large enough to receive the decoded structure, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, in the variable pointed to by <i>pcbStructInfo</i>.

This parameter can be <b>NULL</b> to retrieve the size of this information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbStructInfo [in, out]

A pointer to a <b>DWORD</b> value specifying the size, in bytes, of the buffer pointed to by the <i>pvStructInfo</i> parameter. When the function returns, this <b>DWORD</b> value contains the size of the decoded data copied to <i>pvStructInfo</i>. The size contained in the variable pointed to by <i>pcbStructInfo</i> can indicate a size larger than the decoded structure, as the decoded structure can include pointers to other structures. This size is the sum of the size needed by the decoded structure and other structures pointed to. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Some possible error codes are listed in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_BAD_ENCODE</b></dt>
</dl>
</td>
<td width="60%">
An error was encountered while decoding.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
A decoding function could not be found for the specified <i>dwCertEncodingType</i> and <i>lpszStructType</i>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pvStructInfo</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, in the variable pointed to by <i>pcbStructInfo</i>.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -remarks

When encoding a cryptographic object using the preferred <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobjectex">CryptEncodeObjectEx</a> function, the terminating <b>NULL</b> character is included. When decoding, using the preferred <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobjectex">CryptDecodeObjectEx</a> function, the terminating <b>NULL</b> character is not retained.


#### Examples

For an example that uses this function, see 
<a href="/windows/desktop/SecCrypto/example-c-program-asn1-encoding-and-decoding">Example C Program: ASN.1 Encoding and Decoding</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobjectex">CryptDecodeObjectEx</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Object Encoding and Decoding Functions</a>