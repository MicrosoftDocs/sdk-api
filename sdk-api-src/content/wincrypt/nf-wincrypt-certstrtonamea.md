---
UID: NF:wincrypt.CertStrToNameA
title: CertStrToNameA function (wincrypt.h)
description: Converts a null-terminated X.500 string to an encoded certificate name. (ANSI)
helpviewer_keywords: ["CERT_NAME_STR_COMMA_FLAG", "CERT_NAME_STR_CRLF_FLAG", "CERT_NAME_STR_DISABLE_UTF8_DIR_STR_FLAG", "CERT_NAME_STR_ENABLE_PUNYCODE_FLAG", "CERT_NAME_STR_ENABLE_T61_UNICODE_FLAG", "CERT_NAME_STR_ENABLE_UTF8_UNICODE_FLAG", "CERT_NAME_STR_FORCE_UTF8_DIR_STR_FLAG", "CERT_NAME_STR_NO_PLUS_FLAG", "CERT_NAME_STR_NO_QUOTING_FLAG", "CERT_NAME_STR_REVERSE_FLAG", "CERT_NAME_STR_SEMICOLON_FLAG", "CERT_OID_NAME_STR", "CERT_SIMPLE_NAME_STR", "CERT_X500_NAME_STR", "CRYPT_E_INVALID_IA5_STRING", "CRYPT_E_INVALID_NUMERIC_STRING", "CRYPT_E_INVALID_PRINTABLE_STRING", "CRYPT_E_INVALID_X500_STRING", "CertStrToNameA", "X509_ASN_ENCODING", "wincrypt/CertStrToNameA"]
old-location: security\certstrtoname.htm
tech.root: security
ms.assetid: 8bdfafa6-9833-4689-a155-dff09647ec8d
ms.date: 12/05/2018
ms.keywords: CERT_NAME_STR_COMMA_FLAG, CERT_NAME_STR_CRLF_FLAG, CERT_NAME_STR_DISABLE_UTF8_DIR_STR_FLAG, CERT_NAME_STR_ENABLE_PUNYCODE_FLAG, CERT_NAME_STR_ENABLE_T61_UNICODE_FLAG, CERT_NAME_STR_ENABLE_UTF8_UNICODE_FLAG, CERT_NAME_STR_FORCE_UTF8_DIR_STR_FLAG, CERT_NAME_STR_NO_PLUS_FLAG, CERT_NAME_STR_NO_QUOTING_FLAG, CERT_NAME_STR_REVERSE_FLAG, CERT_NAME_STR_SEMICOLON_FLAG, CERT_OID_NAME_STR, CERT_SIMPLE_NAME_STR, CERT_X500_NAME_STR, CRYPT_E_INVALID_IA5_STRING, CRYPT_E_INVALID_NUMERIC_STRING, CRYPT_E_INVALID_PRINTABLE_STRING, CRYPT_E_INVALID_X500_STRING, CertStrToName, CertStrToName function [Security], CertStrToNameA, CertStrToNameW, X509_ASN_ENCODING, _crypto2_certstrtoname, security.certstrtoname, wincrypt/CertStrToName, wincrypt/CertStrToNameA, wincrypt/CertStrToNameW
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CertStrToNameW (Unicode) and CertStrToNameA (ANSI)
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
 - CertStrToNameA
 - wincrypt/CertStrToNameA
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
 - CertStrToName
 - CertStrToNameA
 - CertStrToNameW
---

# CertStrToNameA function


## -description

The <b>CertStrToName</b> function converts a null-terminated <a href="/windows/desktop/SecGloss/x-gly">X.500</a> string to an encoded certificate name.

## -parameters

### -param dwCertEncodingType [in]

The <a href="/windows/desktop/SecGloss/c-gly">certificate encoding type</a>   that was used to encode the string. The <a href="/windows/desktop/SecGloss/m-gly">message encoding type</a> identifier, contained in the high <b>WORD</b> of this value, is ignored by this function.


This parameter can be the following currently defined certificate encoding type.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="X509_ASN_ENCODING"></a><a id="x509_asn_encoding"></a><dl>
<dt><b>X509_ASN_ENCODING</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
Specifies <a href="/windows/desktop/SecGloss/x-gly">X.509</a> certificate encoding.

</td>
</tr>
</table>

### -param pszX500 [in]

A pointer to the null-terminated X.500 string to be converted. The format of this string is specified by the <i>dwStrType</i> parameter.

This string is expected to be formatted the same as the output from 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certnametostra">CertNameToStr</a> function.

### -param dwStrType [in]

This parameter specifies the type of the string. This parameter also specifies other options for the contents of the string. 

If no flags are combined with the string type specifier, the string can contain a comma (,) or a semicolon (;) as separators in the <a href="/windows/desktop/SecGloss/r-gly">relative distinguished name</a> (RDN) and a plus sign (+) as the separator in multiple RDN values.

Quotation marks ("") are supported. A quotation can be included in a quoted value by using two sets of quotation marks, for example, CN="User ""one""". 

A value that starts with a number sign (#) is treated as <a href="/windows/desktop/SecGloss/a-gly">ASCII</a> hexadecimal and converted to a <b>CERT_RDN_OCTET_STRING</b>. Embedded white space is ignored. For example, 1.2.3 = # AB CD 01 is the same as 1.2.3=#ABCD01.

White space that surrounds the keys, object identifiers, and values is ignored.


This parameter can be one of the following values.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_SIMPLE_NAME_STR"></a><a id="cert_simple_name_str"></a><dl>
<dt><b>CERT_SIMPLE_NAME_STR</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
This string type is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_OID_NAME_STR"></a><a id="cert_oid_name_str"></a><dl>
<dt><b>CERT_OID_NAME_STR</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
 Validates that the string type is supported. The string can be either an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) or an X.500 name.
							

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_X500_NAME_STR"></a><a id="cert_x500_name_str"></a><dl>
<dt><b>CERT_X500_NAME_STR</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Identical to  CERT_OID_NAME_STR. Validates that the string type is supported. The string can be either an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) or an X.500 name.
							

</td>
</tr>
</table>
 


The following options can also be combined with the value above to specify additional options for the string.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_COMMA_FLAG"></a><a id="cert_name_str_comma_flag"></a><dl>
<dt><b>CERT_NAME_STR_COMMA_FLAG</b></dt>
<dt>0x04000000</dt>
</dl>
</td>
<td width="60%">
Only a comma (,) is supported as the RDN separator.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_SEMICOLON_FLAG"></a><a id="cert_name_str_semicolon_flag"></a><dl>
<dt><b>CERT_NAME_STR_SEMICOLON_FLAG</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
Only a semicolon (;) is supported as the RDN separator.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_CRLF_FLAG"></a><a id="cert_name_str_crlf_flag"></a><dl>
<dt><b>CERT_NAME_STR_CRLF_FLAG</b></dt>
<dt>0x08000000</dt>
</dl>
</td>
<td width="60%">
Only a backslash r (\r) or backslash n (\n) is supported as the RDN separator.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_NO_PLUS_FLAG"></a><a id="cert_name_str_no_plus_flag"></a><dl>
<dt><b>CERT_NAME_STR_NO_PLUS_FLAG</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
The plus sign (+) is ignored as a separator, and multiple values per RDN are not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_NO_QUOTING_FLAG"></a><a id="cert_name_str_no_quoting_flag"></a><dl>
<dt><b>CERT_NAME_STR_NO_QUOTING_FLAG</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Quoting is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_REVERSE_FLAG"></a><a id="cert_name_str_reverse_flag"></a><dl>
<dt><b>CERT_NAME_STR_REVERSE_FLAG</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
The order of the RDNs in a distinguished name is reversed before encoding. This flag is not set by default.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_ENABLE_T61_UNICODE_FLAG"></a><a id="cert_name_str_enable_t61_unicode_flag"></a><dl>
<dt><b>CERT_NAME_STR_ENABLE_T61_UNICODE_FLAG</b></dt>
<dt>0x00020000</dt>
</dl>
</td>
<td width="60%">
The <b>CERT_RDN_T61_STRING</b> encoded value type is used instead of <b>CERT_RDN_UNICODE_STRING</b>. This flag can be used if all the Unicode characters are less than or equal to 0xFF.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_ENABLE_UTF8_UNICODE_FLAG"></a><a id="cert_name_str_enable_utf8_unicode_flag"></a><dl>
<dt><b>CERT_NAME_STR_ENABLE_UTF8_UNICODE_FLAG</b></dt>
<dt>0x00040000</dt>
</dl>
</td>
<td width="60%">
The <b>CERT_RDN_UTF8_STRING</b> encoded value type is used instead of <b>CERT_RDN_UNICODE_STRING</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_FORCE_UTF8_DIR_STR_FLAG"></a><a id="cert_name_str_force_utf8_dir_str_flag"></a><dl>
<dt><b>CERT_NAME_STR_FORCE_UTF8_DIR_STR_FLAG</b></dt>
<dt>0x00080000</dt>
</dl>
</td>
<td width="60%">
Forces the X.500 key to be encoded as a UTF-8 (CERT_RDN_UTF8_STRING) string rather than as a printable  Unicode (CERT_RDN_PRINTABLE_STRING) string. This is the default value for Microsoft certification authorities beginning with Windows Server 2003.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_DISABLE_UTF8_DIR_STR_FLAG"></a><a id="cert_name_str_disable_utf8_dir_str_flag"></a><dl>
<dt><b>CERT_NAME_STR_DISABLE_UTF8_DIR_STR_FLAG</b></dt>
<dt>0x00100000</dt>
</dl>
</td>
<td width="60%">
Prevents forcing a printable Unicode (CERT_RDN_PRINTABLE_STRING) X.500 key to be encoded by using UTF-8 (CERT_RDN_UTF8_STRING). Use to enable encoding of X.500 keys as Unicode values when CERT_NAME_STR_FORCE_UTF8_DIR_STR_FLAG is set.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_ENABLE_PUNYCODE_FLAG"></a><a id="cert_name_str_enable_punycode_flag"></a><dl>
<dt><b>CERT_NAME_STR_ENABLE_PUNYCODE_FLAG</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
If the string contains an email RDN value, and the email address  contains Unicode characters outside of the ASCII character set, the host name portion of the email address is encoded in Punycode. The resultant email address is then encoded as an <a href="/windows/desktop/SecCertEnroll/about-ia5string">IA5String</a> string. The Punycode encoding of the host name is performed on a label-by-label basis.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
</table>

### -param pvReserved [in, optional]

Reserved for future use and must be <b>NULL</b>.

### -param pbEncoded [out]

A pointer to a buffer that receives the encoded structure. 


The size of this buffer is specified in the <i>pcbEncoded</i> parameter.

This parameter can be <b>NULL</b> to obtain the required size of the buffer for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbEncoded [in, out]

A pointer to a <b>DWORD</b> that, before calling the function, contains the size, in bytes, of the buffer pointed to by the <i>pbEncoded</i> parameter. When the function returns, the <b>DWORD</b> contains the number of bytes stored in the buffer.

If <i>pbEncoded</i> is <b>NULL</b>, the <b>DWORD</b> receives the size, in bytes, required for the buffer.

### -param ppszError [out, optional]

A pointer to a string pointer that receives additional error information about an input string that is not valid. 


If the <i>pszX500</i> string is not valid, <i>ppszError</i> is updated by this function to point to the beginning of the character sequence that is not valid. If no errors are detected in the input string, <i>ppszError</i> is set to <b>NULL</b>.
						

If this information is not required, pass <b>NULL</b> for this parameter.


This parameter is updated for the following error codes returned from <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.



<a id="CRYPT_E_INVALID_X500_STRING"></a>
<a id="crypt_e_invalid_x500_string"></a>


#### CRYPT_E_INVALID_X500_STRING

<a id="CRYPT_E_INVALID_NUMERIC_STRING"></a>
<a id="crypt_e_invalid_numeric_string"></a>


#### CRYPT_E_INVALID_NUMERIC_STRING

<a id="CRYPT_E_INVALID_PRINTABLE_STRING"></a>
<a id="crypt_e_invalid_printable_string"></a>


#### CRYPT_E_INVALID_PRINTABLE_STRING

<a id="CRYPT_E_INVALID_IA5_STRING"></a>
<a id="crypt_e_invalid_ia5_string"></a>


#### CRYPT_E_INVALID_IA5_STRING

## -returns

Returns nonzero if successful or zero otherwise.
						

For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The following table contains the supported X.500 keys, their corresponding object identifier string, string identifier (from Wincrypt.h), and value types.

<table>
<tr>
<th>Key</th>
<th>Object identifier string</th>
<th>String identifier</th>
<th>RDN value types</th>
</tr>
<tr>
<td>
CN

</td>
<td>
2.5.4.3

</td>
<td>
szOID_COMMON_NAME

</td>
<td>
Printable

T61

</td>
</tr>
<tr>
<td>
L

</td>
<td>
2.5.4.7

</td>
<td>
szOID_LOCALITY_NAME

</td>
<td>
Printable

T61

</td>
</tr>
<tr>
<td>
O

</td>
<td>
2.5.4.10

</td>
<td>
szOID_ORGANIZATION_NAME

</td>
<td>
Printable

T61

</td>
</tr>
<tr>
<td>
OU

</td>
<td>
2.5.4.11

</td>
<td>
szOID_ORGANIZATIONAL_UNIT_NAME

</td>
<td>
Printable

T61

</td>
</tr>
<tr>
<td>
E

Email

</td>
<td>
1.2.840.113549.1.9.1

</td>
<td>
szOID_RSA_emailAddr

</td>
<td>
IA5

</td>
</tr>
<tr>
<td>
C

</td>
<td>
2.5.4.6

</td>
<td>
szOID_COUNTRY_NAME

</td>
<td>
Printable

</td>
</tr>
<tr>
<td>
S

ST

</td>
<td>
2.5.4.8

</td>
<td>
szOID_STATE_OR_PROVINCE_NAME

</td>
<td>
Printable

T61

</td>
</tr>
<tr>
<td>
STREET

</td>
<td>
2.5.4.9

</td>
<td>
szOID_STREET_ADDRESS

</td>
<td>
Printable

T61

</td>
</tr>
<tr>
<td>
T

Title

</td>
<td>
2.5.4.12

</td>
<td>
szOID_TITLE

</td>
<td>
Printable

T61

</td>
</tr>
<tr>
<td>
G

GivenName

</td>
<td>
2.5.4.42

</td>
<td>
szOID_GIVEN_NAME

</td>
<td>
Printable

T61

</td>
</tr>
<tr>
<td>
I

Initials

</td>
<td>
2.5.4.43

</td>
<td>
szOID_INITIALS

</td>
<td>
Printable

T61

</td>
</tr>
<tr>
<td>
SN

</td>
<td>
2.5.4.4

</td>
<td>
szOID_SUR_NAME

</td>
<td>
Printable

T61

</td>
</tr>
<tr>
<td>
DC

</td>
<td>
0.9.2342.19200300.100.1.25

</td>
<td>
szOID_DOMAIN_COMPONENT

</td>
<td>
IA5

UTF8

</td>
</tr>
</table>
 


If either Printable or T61 is allowed as the RDN value type for the key, Printable is automatically selected if the name string component is a member of the following character sets:

<ul>
<li>A, B, …, Z</li>
<li>a, b, …, z</li>
<li>0, 1, …, 9</li>
<li>(space) ' ( ) + , - . / : = ?</li>
</ul>


The T61 types are UTF8 encoded.


#### Examples

For an example that uses this function, see 
<a href="/windows/desktop/SecCrypto/example-c-program-converting-names-from-certificates-to-asn1-and-back">Example C Program: Converting Names from Certificates to ASN.1 and Back</a>.

<div class="code"></div>




> [!NOTE]
> The wincrypt.h header defines CertStrToName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certnametostra">CertNameToStr</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Conversion Functions</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>
