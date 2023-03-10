---
UID: NF:wincrypt.CryptDecodeObjectEx
title: CryptDecodeObjectEx function (wincrypt.h)
description: Decodes a structure of the type indicated by the lpszStructType parameter.
helpviewer_keywords: ["CRYPT_DECODE_ALLOC_FLAG","CRYPT_DECODE_ENABLE_PUNYCODE_FLAG","CRYPT_DECODE_NOCOPY_FLAG","CRYPT_DECODE_NO_SIGNATURE_BYTE_REVERSAL_FLAG","CRYPT_DECODE_SHARE_OID_STRING_FLAG","CRYPT_DECODE_TO_BE_SIGNED_FLAG","CRYPT_UNICODE_NAME_DECODE_DISABLE_IE4_UTF8_FLAG","CryptDecodeObjectEx","CryptDecodeObjectEx function [Security]","_crypto2_cryptdecodeobjectex","security.cryptdecodeobjectex","wincrypt/CryptDecodeObjectEx"]
old-location: security\cryptdecodeobjectex.htm
tech.root: security
ms.assetid: bf1935f0-1ab0-4068-9ed5-8fbb2c286b8a
ms.date: 12/05/2018
ms.keywords: CRYPT_DECODE_ALLOC_FLAG, CRYPT_DECODE_ENABLE_PUNYCODE_FLAG, CRYPT_DECODE_NOCOPY_FLAG, CRYPT_DECODE_NO_SIGNATURE_BYTE_REVERSAL_FLAG, CRYPT_DECODE_SHARE_OID_STRING_FLAG, CRYPT_DECODE_TO_BE_SIGNED_FLAG, CRYPT_UNICODE_NAME_DECODE_DISABLE_IE4_UTF8_FLAG, CryptDecodeObjectEx, CryptDecodeObjectEx function [Security], _crypto2_cryptdecodeobjectex, security.cryptdecodeobjectex, wincrypt/CryptDecodeObjectEx
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
 - CryptDecodeObjectEx
 - wincrypt/CryptDecodeObjectEx
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
 - CryptDecodeObjectEx
---

# CryptDecodeObjectEx function


## -description

The <b>CryptDecodeObjectEx</b> function decodes a structure of the type indicated by the <i>lpszStructType</i> parameter. <b>CryptDecodeObjectEx</b> offers a significant performance improvement over 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a> by supporting memory allocation with the CRYPT_DECODE_ALLOC_FLAG value.

## -parameters

### -param dwCertEncodingType [in]

The type of encoding used. It is always acceptable to specify both the <a href="/windows/desktop/SecGloss/c-gly">certificate</a> and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING

Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>
<div class="alert"><b>Note</b>  Either a certificate or message encoding type is required. X509_ASN_ENCODING is the default. If that type is indicated, it is used. Otherwise, if the PKCS7_ASN_ENCODING type is indicated, it is used.</div>
<div> </div>

### -param lpszStructType [in]

A pointer to an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) that defines the structure type. If the high-order word of the <i>lpszStructType</i> parameter is zero, the low-order word specifies the integer identifier for the type of the specified structure. Otherwise, this parameter is a long pointer to a null-terminated string.

For more information about object identifier strings, their predefined constants, and corresponding structures, see 
<a href="/windows/desktop/SecCrypto/constants-for-cryptencodeobject-and-cryptdecodeobject">Constants for CryptEncodeObject and CryptDecodeObject</a>.

### -param pbEncoded [in]

A pointer to the data to be decoded. The structure must be of the type specified by <i>lpszStructType</i>.

### -param cbEncoded [in]

The number of bytes pointed to by <i>pbEncoded</i>. This is the number of bytes to be decoded.

### -param dwFlags [in]

This parameter can be one or more of the following flags. The flags can be combined by using a bitwise-<b>OR</b> operation.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DECODE_ALLOC_FLAG"></a><a id="crypt_decode_alloc_flag"></a><dl>
<dt><b>CRYPT_DECODE_ALLOC_FLAG</b></dt>
</dl>
</td>
<td width="60%">
The called decoding function allocates memory for the decoded structure. A pointer to the allocated structure is returned in <i>pvStructInfo</i>.

If <i>pDecodePara</i> or the <b>pfnAlloc</b>  member of <i>pDecodePara</i> is <b>NULL</b>, then <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> is called for the allocation and <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> must be called to free the memory.

If <i>pDecodePara</i> and the <b>pfnAlloc</b>  member of <i>pDecodePara</i> are not <b>NULL</b>, then the function pointed to by <b>pfnAlloc</b> is called for the allocation and the function pointed to by the <b>pfnFree</b>  member of <i>pDecodePara</i> must be called to free the memory.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DECODE_ENABLE_PUNYCODE_FLAG"></a><a id="crypt_decode_enable_punycode_flag"></a><dl>
<dt><b>CRYPT_DECODE_ENABLE_PUNYCODE_FLAG</b></dt>
<dt>33554432 (0x2000000)</dt>
</dl>
</td>
<td width="60%">
This flag is applicable for enabling Punycode decoding of Unicode string values. For more information, see Remarks.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DECODE_NOCOPY_FLAG"></a><a id="crypt_decode_nocopy_flag"></a><dl>
<dt><b>CRYPT_DECODE_NOCOPY_FLAG</b></dt>
</dl>
</td>
<td width="60%">
This flag can be set to enable a "no copy" optimization. This optimization updates the <i>pvStructInfo</i> members to point to content that resides within <i>pbEncoded</i> instead of making a copy of the content and appending it to <i>pvStructInfo</i>. The calling application needs to allocate less memory and execution is faster because a copy is not made. Note that when performing "no copy" decoding, <i>pbEncoded</i> cannot be freed until <i>pvStructInfo</i> is freed.

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

### -param pDecodePara [in]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_decode_para">CRYPT_DECODE_PARA</a> structure that contains decoding paragraph information. If <i>pDecodePara</i> is set to <b>NULL</b>, then <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> and <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> are used to allocate and free memory. If <i>pDecodePara</i> points to a <b>CRYPT_DECODE_PARA</b> structure, that structure passes in callback functions to allocate and free memory. These callback functions override the default memory allocation of <b>LocalAlloc</b> and <b>LocalFree</b>.

### -param pvStructInfo [out]

If the <i>dwFlags</i> CRYPT_ENCODE_ALLOC_FLAG is set, <i>pvStructInfo</i> is not a pointer to a buffer but is the address of a pointer to the buffer. Because memory is allocated inside the function and the pointer is stored at *<i>pvStructInfo</i>, <i>pvStructInfo</i> must never be <b>NULL</b>.

If CRYPT_ENCODE_ALLOC_FLAG is not set, <i>pvStructInfo</i> is a pointer to a buffer that receives the decoded structure. When the buffer that is specified is not large enough to receive the decoded structure, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, in the variable pointed to by <i>pcbStructInfo</i>.

This parameter can be <b>NULL</b> to retrieve the size of this information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbStructInfo [in, out]

A pointer to a <b>DWORD</b> variable that contains the size, in bytes, of the buffer pointed to by the <i>pvStructInfo</i> parameter. When the function returns, the <b>DWORD</b> value contains the number of bytes stored in the buffer. The size contained in the variable pointed to by <i>pcbStructInfo</i> can indicate a size larger than the decoded structure because the decoded structure can include pointers to auxiliary data. This size is the sum of the size needed by the decoded structure and the auxiliary data.

When CRYPT_DECODE_ALLOC_FLAG is set, the initial value of *<i>pcbStructInfo</i> is not used by the function, and on return, *<i>pcbStructInfo</i> contains the number of bytes allocated for <i>pvStructInfo</i>.

<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following table shows some possible error codes.

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
A decoding function could not be found for the specified <i>dwCertEncodingType</i> and <i>lpszStructType</i>.
							

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
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -remarks

When encoding a cryptographic object using the preferred <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobjectex">CryptEncodeObjectEx</a> function, the terminating <b>NULL</b> character is included. When decoding, using the preferred <b>CryptDecodeObjectEx</b> function, the terminating <b>NULL</b> character is not retained.

Each constant in the list below has an associated structure type that is pointed to by the <i>pvStructInfo</i> parameter. The structure  pointed to, directly or indirectly, has a reference to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_entry">CERT_ALT_NAME_ENTRY</a> structure.  

<ul>
<li>X509_ALTERNATE_NAME
	</li>
<li>szOID_AUTHORITY_INFO_ACCESS
			</li>
<li>X509_AUTHORITY_INFO_ACCESS
			</li>
<li>X509_AUTHORITY_KEY_ID2
			</li>
<li>szOID_AUTHORITY_KEY_IDENTIFIER2
			</li>
<li>szOID_CRL_DIST_POINTS
			</li>
<li>X509_CRL_DIST_POINTS
			</li>
<li>szOID_CROSS_CERT_DIST_POINTS
			</li>
<li>X509_CROSS_CERT_DIST_POINTS
			</li>
<li>szOID_ISSUER_ALT_NAME
			</li>
<li>szOID_ISSUER_ALT_NAME2
			</li>
<li>szOID_ISSUING_DIST_POINT
	</li>
<li>X509_ISSUING_DIST_POINT
			</li>
<li>X509_NAME_CONSTRAINTS
			</li>
<li>szOID_NAME_CONSTRAINTS
			</li>
<li>szOID_NEXT_UPDATE_LOCATION
			</li>
<li>OCSP_REQUEST
			</li>
<li>zOID_SUBJECT_ALT_NAME
			</li>
<li>szOID_SUBJECT_ALT_NAME2
			</li>
</ul>
The <b>CRYPT_DECODE_ENABLE_PUNYCODE_FLAG</b> flag, in conjunction with the value of the <b>dwAltNameChoice</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_entry">CERT_ALT_NAME_ENTRY</a> structure, determines the manner in which strings are encoded.

<table>
<tr>
<th><b>dwAltNameChoice</b></th>
<th>Effect</th>
</tr>
<tr>
<td><b>CERT_ALT_NAME_DNS_NAME</b></td>
<td>If the host name contains a Punycode encoded <a href="/windows/desktop/SecCertEnroll/about-ia5string">IA5String</a> string, it is converted  to the  Unicode equivalent.</td>
</tr>
<tr>
<td><b>CERT_ALT_NAME_RFC822_NAME</b></td>
<td>If the host name portion of the email address contains a Punycode encoded <a href="/windows/desktop/SecCertEnroll/about-ia5string">IA5String</a> string, it is converted to its Unicode equivalent.</td>
</tr>
<tr>
<td><b>CERT_ALT_NAME_URL</b></td>
<td>The URI is decoded. If the server host name of the URI contains a Punycode encoded <a href="/windows/desktop/SecCertEnroll/about-ia5string">IA5String</a> string, the host name string  is decoded to the Unicode equivalent.</td>
</tr>
</table>
 

Each constant in the list below has an associated structure type that is pointed to by the <i>pvStructInfo</i> parameter. The structure  pointed to, directly or indirectly, has a reference to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_hashed_url">CERT_HASHED_URL</a> structure. 

<ul>
<li>szOID_LOGOTYPE_EXT</li>
<li>X509_LOGOTYPE_EXT</li>
<li>szOID_BIOMETRIC_EXT</li>
<li>X509_BIOMETRIC_EXT</li>
</ul>
When decoding the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_hashed_url">CERT_HASHED_URL</a>  structure value, the URI is decoded.  If the host name contains a Punycode encoded host name, it is converted to the Unicode equivalent.

Each <b>X509_UNICODE_NAME</b> constant in the list below has an associated structure type that is pointed to by the <i>pvStructInfo</i> parameter.

<ul>
<li>X509_UNICODE_NAME</li>
</ul>
If the <i>pszObjId</i> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> structure is set to <b>szOID_RSA_emailAddr</b> and the email address in the <b>Value</b> member contains Punycode encoded string, it is converted to the Unicode equivalent.


#### Examples

For an example that uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-asn1-encoding-and-decoding">Example C Program: ASN.1 Encoding and Decoding</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobjectex">CryptEncodeObjectEx</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Object Encoding and Decoding Functions</a>