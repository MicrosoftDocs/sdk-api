---
UID: NF:wincrypt.CryptEncodeObjectEx
title: CryptEncodeObjectEx function (wincrypt.h)
description: Encodes a structure of the type indicated by the value of the lpszStructType parameter.
helpviewer_keywords: ["CRYPT_ENCODE_ALLOC_FLAG","CRYPT_ENCODE_ENABLE_PUNYCODE_FLAG","CRYPT_UNICODE_NAME_ENCODE_DISABLE_CHECK_TYPE_FLAG","CRYPT_UNICODE_NAME_ENCODE_ENABLE_T61_UNICODE_FLAG","CRYPT_UNICODE_NAME_ENCODE_ENABLE_UTF8_UNICODE_FLAG","CRYPT_UNICODE_NAME_ENCODE_FORCE_UTF8_UNICODE_FLAG","CryptEncodeObjectEx","CryptEncodeObjectEx function [Security]","PKCS_7_ASN_ENCODING","X509_ASN_ENCODING","_crypto2_cryptencodeobjectex","security.cryptencodeobjectex","wincrypt/CryptEncodeObjectEx"]
old-location: security\cryptencodeobjectex.htm
tech.root: security
ms.assetid: 45134db8-059b-43d3-90c2-9b6cc970fca0
ms.date: 12/05/2018
ms.keywords: CRYPT_ENCODE_ALLOC_FLAG, CRYPT_ENCODE_ENABLE_PUNYCODE_FLAG, CRYPT_UNICODE_NAME_ENCODE_DISABLE_CHECK_TYPE_FLAG, CRYPT_UNICODE_NAME_ENCODE_ENABLE_T61_UNICODE_FLAG, CRYPT_UNICODE_NAME_ENCODE_ENABLE_UTF8_UNICODE_FLAG, CRYPT_UNICODE_NAME_ENCODE_FORCE_UTF8_UNICODE_FLAG, CryptEncodeObjectEx, CryptEncodeObjectEx function [Security], PKCS_7_ASN_ENCODING, X509_ASN_ENCODING, _crypto2_cryptencodeobjectex, security.cryptencodeobjectex, wincrypt/CryptEncodeObjectEx
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
 - CryptEncodeObjectEx
 - wincrypt/CryptEncodeObjectEx
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
 - CryptEncodeObjectEx
---

# CryptEncodeObjectEx function


## -description

The <b>CryptEncodeObjectEx</b> function encodes a structure of the type indicated by the value of the <i>lpszStructType</i> parameter. This function offers a significant performance improvement over 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> by supporting memory allocation with the <b>CRYPT_ENCODE_ALLOC_FLAG</b> value.

## -parameters

### -param dwCertEncodingType [in]

The <a href="/windows/desktop/SecGloss/c-gly">certificate encoding type</a> and <a href="/windows/desktop/SecGloss/m-gly">message encoding type</a> to use to encode the object. This parameter can be a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PKCS_7_ASN_ENCODING"></a><a id="pkcs_7_asn_encoding"></a><dl>
<dt><b>PKCS_7_ASN_ENCODING</b></dt>
<dt>65536 (0x10000)</dt>
</dl>
</td>
<td width="60%">
Specifies PKCS 7 message encoding.

</td>
</tr>
<tr>
<td width="40%"><a id="X509_ASN_ENCODING"></a><a id="x509_asn_encoding"></a><dl>
<dt><b>X509_ASN_ENCODING</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Specifies X.509 certificate encoding.

</td>
</tr>
</table>

### -param lpszStructType [in]

A pointer to an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) that defines the structure type. If the high-order word of the <i>lpszStructType</i> parameter is zero, the low-order word specifies an integer identifier for the type of the specified structure. Otherwise, this parameter is a pointer to a null-terminated string that contains the string representation of the OID.

For more information about object identifier strings, their predefined constants and corresponding structures, see 
<a href="/windows/desktop/SecCrypto/constants-for-cryptencodeobject-and-cryptdecodeobject">Constants for CryptEncodeObject and CryptDecodeObject</a>.

### -param pvStructInfo [in]

A pointer to the structure to be encoded. The structure must be of the type specified by <i>lpszStructType</i>.

### -param dwFlags [in]

Specifies options for the encoding. This parameter can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ENCODE_ALLOC_FLAG"></a><a id="crypt_encode_alloc_flag"></a><dl>
<dt><b>CRYPT_ENCODE_ALLOC_FLAG</b></dt>
<dt>32768 (0x8000)</dt>
</dl>
</td>
<td width="60%">
The called encoding function allocates memory for the encoded bytes. A pointer to the allocated bytes is returned in <i>pvEncoded</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ENCODE_ENABLE_PUNYCODE_FLAG"></a><a id="crypt_encode_enable_punycode_flag"></a><dl>
<dt><b>CRYPT_ENCODE_ENABLE_PUNYCODE_FLAG</b></dt>
<dt>131072 (0x20000)</dt>
</dl>
</td>
<td width="60%">
This flag is applicable for enabling Punycode encoding of Unicode string values. For more information, see Remarks.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This flag is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_UNICODE_NAME_ENCODE_DISABLE_CHECK_TYPE_FLAG"></a><a id="crypt_unicode_name_encode_disable_check_type_flag"></a><dl>
<dt><b>CRYPT_UNICODE_NAME_ENCODE_DISABLE_CHECK_TYPE_FLAG</b></dt>
<dt>1073741824 (0x40000000)</dt>
</dl>
</td>
<td width="60%">
This flag is applicable when encoding X509_UNICODE_NAME, X509_UNICODE_NAME_VALUE, or X509_UNICODE_ANY_STRING. If this flag is set, the characters are not checked to determine whether they are valid for the specified value type.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_UNICODE_NAME_ENCODE_ENABLE_T61_UNICODE_FLAG"></a><a id="crypt_unicode_name_encode_enable_t61_unicode_flag"></a><dl>
<dt><b>CRYPT_UNICODE_NAME_ENCODE_ENABLE_T61_UNICODE_FLAG</b></dt>
<dt>2147483648 (0x80000000)</dt>
</dl>
</td>
<td width="60%">
This flag is applicable when encoding X509_UNICODE_NAME. If this flag is set and all the Unicode characters are &lt;= 0xFF, the CERT_RDN_T61_STRING is selected instead of the CERT_RDN_UNICODE_STRING.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_UNICODE_NAME_ENCODE_ENABLE_UTF8_UNICODE_FLAG"></a><a id="crypt_unicode_name_encode_enable_utf8_unicode_flag"></a><dl>
<dt><b>CRYPT_UNICODE_NAME_ENCODE_ENABLE_UTF8_UNICODE_FLAG</b></dt>
<dt>536870912 (0x20000000)</dt>
</dl>
</td>
<td width="60%">
This flag is applicable when encoding an X509_UNICODE_NAME. When set, CERT_RDN_UTF8_STRING is selected instead of CERT_RDN_UNICODE_STRING.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_UNICODE_NAME_ENCODE_FORCE_UTF8_UNICODE_FLAG_"></a><a id="crypt_unicode_name_encode_force_utf8_unicode_flag_"></a><dl>
<dt><b>CRYPT_UNICODE_NAME_ENCODE_FORCE_UTF8_UNICODE_FLAG </b></dt>
<dt>268435456 (0x10000000)</dt>
</dl>
</td>
<td width="60%">
This flag is applicable when encoding an X509_UNICODE_NAME. When set, CERT_RDN_UTF8_STRING is selected instead of CERT_RDN_PRINTABLE_STRING for directory string types. Also, this flag enables CRYPT_UNICODE_NAME_ENCODE_ENABLE_UTF8_UNICODE_FLAG.

</td>
</tr>
</table>

### -param pEncodePara [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_encode_para">CRYPT_ENCODE_PARA</a> structure that contains encoding information. This parameter can be <b>NULL</b>.

If either <i>pEncodePara</i> or the <b>pfnAlloc</b> member of <i>pEncodePara</i> is <b>NULL</b>, then <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> is used for the allocation and <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> must be called to free the memory.

If both <i>pEncodePara</i> and the <b>pfnAlloc</b> member of <i>pEncodePara</i> are not <b>NULL</b>, then the function pointed to by the <b>pfnAlloc</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_encode_para">CRYPT_ENCODE_PARA</a> structure pointed to by <i>pEncodePara</i> is called for the allocation. The function pointed to by the <b>pfnFree</b> member of <i>pEncodePara</i> must be called to free the memory.

### -param pvEncoded [out]

A pointer to a buffer to receive the encoded structure. The size of this buffer is specified in the <i>pcbEncoded</i> parameter. When the buffer that is specified is not large enough to receive the decoded structure, the function sets the <b>ERROR_MORE_DATA</b> code and stores the required buffer size, in bytes, in the variable pointed to by <i>pcbEncoded</i>.

This parameter can be <b>NULL</b> to retrieve the size of the buffer for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

If <i>dwFlags</i> contains the <b>CRYPT_ENCODE_ALLOC_FLAG</b> flag, <i>pvEncoded</i> is not a pointer to a buffer but is the address of a pointer to the buffer. Because memory is allocated inside the function and the pointer is stored in <i>pvEncoded</i>, <i>pvEncoded</i> cannot be <b>NULL</b>.

### -param pcbEncoded [in, out]

A pointer to a <b>DWORD</b> variable that contains the size, in bytes, of the buffer pointed to by the <i>pvEncoded</i> parameter. When the function returns, the variable pointed to by the <i>pcbEncoded</i> parameter contains the number of allocated, encoded bytes stored in the buffer.

When <i>dwFlags</i> contains the <b>CRYPT_ENCODE_ALLOC_FLAG</b> flag, <i>pcbEncoded</i> is the address of a pointer to the <b>DWORD</b> value that is updated.

<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

Returns nonzero if successful or zero otherwise.

For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. The following table shows some possible error codes that can be returned from <b>GetLastError</b> when <b>CryptEncodeObjectEx</b> fails.

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
An error was encountered while encoding.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
An encoding function could not be found for the specified <i>dwCertEncodingType</i> and <i>lpszStructType</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pvEncoded</i> parameter is not large enough to hold the returned data, the function sets the <b>ERROR_MORE_DATA</b> code and stores the required buffer size, in bytes, in the variable pointed to by <i>pcbEncoded</i>.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -remarks

When encoding a cryptographic object using the preferred <b>CryptEncodeObjectEx</b> function, the terminating <b>NULL</b> character is included. When decoding, using the preferred <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobjectex">CryptDecodeObjectEx</a> function, the terminating <b>NULL</b> character is not retained.

<b>CryptEncodeObjectEx</b> first looks for an installable extended encoding function. If no extended encoding function is found, the old, nonextended, installable function is located.

 When direct <a href="/windows/desktop/SecCertEnroll/about-ia5string">IA5String</a> encoding of the object is not possible, you can specify Punycode encoding by setting the <i>dwFlag</i> parameter to the <b>CRYPT_ENCODE_ENABLE_PUNYCODE_FLAG</b> value. Setting the <b>CRYPT_ENCODE_ENABLE_PUNYCODE_FLAG</b> flag has different effects based on the structure type being encoded as specified by the value of the <i>lpszStructType</i> parameter.

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
<li>szOID_NAME_CONSTRAINTS
			</li>
<li>X509_NAME_CONSTRAINTS
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
The <b>CRYPT_ENCODE_ENABLE_PUNYCODE_FLAG</b> flag, in conjunction with the value of the <b>dwAltNameChoice</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_entry">CERT_ALT_NAME_ENTRY</a> structure, determines the manner in which strings are encoded.

<table>
<tr>
<th><b>dwAltNameChoice</b></th>
<th>Effect</th>
</tr>
<tr>
<td><b>CERT_ALT_NAME_DNS_NAME</b></td>
<td>If the host name contains Unicode characters outside of the ASCII character set, the host name is first encoded in Punycode and then encoded as an <a href="/windows/desktop/SecCertEnroll/about-ia5string">IA5String</a> string. </td>
</tr>
<tr>
<td><b>CERT_ALT_NAME_RFC822_NAME</b></td>
<td>If the host name portion of the email address contains Unicode characters outside of the ASCII character set, the host name portion of the email address is encoded in Punycode. The resultant email address is then encoded as an <a href="/windows/desktop/SecCertEnroll/about-ia5string">IA5String</a> string. </td>
</tr>
<tr>
<td><b>CERT_ALT_NAME_URL</b></td>
<td>If the server host name of the URI contains Unicode characters outside of the ASCII character set,  then the host name portion of URI is encoded in Punycode. Then the resultant URI is escaped, and the URL is then  encoded as an <a href="/windows/desktop/SecCertEnroll/about-ia5string">IA5String</a> string. </td>
</tr>
</table>
 

Each constant in the list below has an associated structure type that is pointed to by the <i>pvStructInfo</i> parameter. The structure  pointed to, directly or indirectly, has a reference to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_hashed_url">CERT_HASHED_URL</a> structure. 

<ul>
<li>szOID_BIOMETRIC_EXT</li>
<li>X509_BIOMETRIC_EXT</li>
<li>szOID_LOGOTYPE_EXT</li>
<li>X509_LOGOTYPE_EXT</li>
</ul>
When encoding the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_hashed_url">CERT_HASHED_URL</a> structure value, if the server host name of the URI contains Unicode characters outside of the ASCII character set, and the <b>CRYPT_ENCODE_ENABLE_PUNYCODE_FLAG</b> is set, the host name portion of URI is encoded in Punycode.  Then the resultant URI is escaped, and the URL is then  encoded as an <a href="/windows/desktop/SecCertEnroll/about-ia5string">IA5String</a> string.

Each <b>X509_UNICODE_NAME</b> constant in the list below has an associated structure type that is pointed to by the <i>pvStructInfo</i> parameter.

<ul>
<li>X509_UNICODE_NAME</li>
</ul>
If the <i>pszObjId</i> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> structure is set to <b>szOID_RSA_emailAddr</b> and the email address in the <b>Value</b> member contains Unicode characters outside of the ASCII character set, the host name portion of the email address is encoded in Punycode. Then the resultant email address is then  encoded as an <a href="/windows/desktop/SecCertEnroll/about-ia5string">IA5String</a> string.

In all cases, the Punycode encoding of the host name is performed on a label-by-label basis.


#### Examples

The following example shows initializing and encoding an X509_NAME structure using <b>CryptEncodeObjectEx</b>. For an example that includes the complete context for this example, see <a href="/windows/desktop/SecCrypto/example-c-program-asn1-encoding-and-decoding">Example C Program: ASN.1 Encoding and Decoding</a>.


```cpp
#include <windows.h>
#include <stdio.h>
#include <Wincrypt.h>
#pragma comment(lib, "crypt32.lib")


#define MY_TYPE (X509_ASN_ENCODING)

void main()
{

//#define moved

//--------------------------------------------------------------------
//   Declare and initialize local variables.

char *Cert_Sub_Name ="Test User Name";

//--------------------------------------------------------------------
// Initialize a single RDN structure.

CERT_RDN_ATTR rgNameAttr = 
{
   "2.5.4.3",                      // The OID
   CERT_RDN_PRINTABLE_STRING,      // Type of string
   (DWORD)strlen(Cert_Sub_Name)+1, // String length including
                                   //  the terminating null character
   (BYTE *)Cert_Sub_Name           // Pointer to the string 
};
//--------------------------------------------------------------------
// Declare and initialize a structure to include
// the array of RDN structures.

CERT_RDN rgRDN[] = 
{
   1,               // The number of elements in the array
   &rgNameAttr      // Pointer to the array
};

//--------------------------------------------------------------------
//  Declare and initialize a CERT_NAME_INFO 
//  structure that includes a CERT_RND.

CERT_NAME_INFO CertName = 
{
    1,          // The number of elements in the CERT_RND's array
    rgRDN
};

//--------------------------------------------------------------------
//  Declare additional variables.

DWORD cbEncoded;              // Variable to hold the
                              //  length of the encoded string
BYTE *pbEncoded;              // Variable to hold a pointer to the 
                              //  encoded buffer
//--------------------------------------------------------------------
// Call CrypteEncodeObjectEx to get 
// length to allocate for pbEncoded.

if( CryptEncodeObjectEx(
     MY_TYPE,        // The encoding/decoding type
     X509_NAME,    
     &CertName,
     0,                 
     NULL, 
     NULL,
     &cbEncoded))    // Fill in the length needed for
                     // the encoded buffer.
{
     printf("The number of bytes needed is %d \n",cbEncoded);
}
else
{
     printf("The first call to the function failed.\n");
     exit(1);
}

if( pbEncoded = (BYTE*)malloc(cbEncoded))
{
     printf("Memory for pvEncoded has been allocated.\n");
}
else
{
    printf("Memory allocation failed.\n");
    exit(1);
}

if(CryptEncodeObjectEx(
     MY_TYPE,
     X509_NAME,
     &CertName,
     0,
     NULL, 
     pbEncoded,
     &cbEncoded))
{
     printf("The structure has been encoded.\n");
}
else
{
     printf("Encoding failed.");
     exit(1);
}
// Free allocated memory when done.
// ...
if(pbEncoded)
{
    free(pbEncoded);
}


```

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobjectex">CryptDecodeObjectEx</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Object Encoding and Decoding Functions</a>