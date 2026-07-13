---
UID: NF:wincrypt.CertNameToStrW
title: CertNameToStrW function (wincrypt.h)
description: Converts an encoded name in a CERT_NAME_BLOB structure to a null-terminated character string. (Unicode)
helpviewer_keywords: ["CERT_NAME_STR_CRLF_FLAG", "CERT_NAME_STR_DISABLE_IE4_UTF8_FLAG", "CERT_NAME_STR_ENABLE_PUNYCODE_FLAG", "CERT_NAME_STR_NO_PLUS_FLAG", "CERT_NAME_STR_NO_QUOTING_FLAG", "CERT_NAME_STR_REVERSE_FLAG", "CERT_NAME_STR_SEMICOLON_FLAG", "CERT_OID_NAME_STR", "CERT_SIMPLE_NAME_STR", "CERT_X500_NAME_STR", "CertNameToStr", "CertNameToStr function [Security]", "CertNameToStrW", "X509_ASN_ENCODING", "_crypto2_certnametostr", "security.certnametostr", "wincrypt/CertNameToStr", "wincrypt/CertNameToStrW"]
old-location: security\certnametostr.htm
tech.root: security
ms.assetid: b3d96de8-5cbc-4ccb-b759-6757520bbda3
ms.date: 12/05/2018
ms.keywords: CERT_NAME_STR_CRLF_FLAG, CERT_NAME_STR_DISABLE_IE4_UTF8_FLAG, CERT_NAME_STR_ENABLE_PUNYCODE_FLAG, CERT_NAME_STR_NO_PLUS_FLAG, CERT_NAME_STR_NO_QUOTING_FLAG, CERT_NAME_STR_REVERSE_FLAG, CERT_NAME_STR_SEMICOLON_FLAG, CERT_OID_NAME_STR, CERT_SIMPLE_NAME_STR, CERT_X500_NAME_STR, CertNameToStr, CertNameToStr function [Security], CertNameToStrA, CertNameToStrW, X509_ASN_ENCODING, _crypto2_certnametostr, security.certnametostr, wincrypt/CertNameToStr, wincrypt/CertNameToStrA, wincrypt/CertNameToStrW
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CertNameToStrW (Unicode) and CertNameToStrA (ANSI)
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
 - CertNameToStrW
 - wincrypt/CertNameToStrW
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
 - CertNameToStr
 - CertNameToStrA
 - CertNameToStrW
---

# CertNameToStrW function


## -description

The <b>CertNameToStr</b> function converts an encoded name in a 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> structure to a null-terminated character string.

The string representation follows the distinguished name specifications in <a href="https://www.ietf.org/rfc/rfc1779.txt">RFC 1779</a>. The exceptions to this rule are listed in the Remarks section, below.

## -parameters

### -param dwCertEncodingType [in]

The <a href="/windows/desktop/SecGloss/c-gly">certificate encoding type</a>   that was used to encode the name. The <a href="/windows/desktop/SecGloss/m-gly">message encoding type</a> identifier, contained in the high <b>WORD</b> of this value, is ignored by this function.


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
Specifies X.509 certificate encoding.

</td>
</tr>
</table>

### -param pName [in]

A pointer to the 
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> structure to be converted.

### -param dwStrType [in]

This parameter specifies the format of the output string. This parameter also specifies other options for the contents of the string.


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
All <a href="/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs) are discarded. 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn">CERT_RDN</a> entries are separated by a comma followed by a space (, ). Multiple attributes in a <b>CERT_RDN</b> are separated by a plus sign enclosed within spaces ( + ),  for example, Microsoft, Kim Abercrombie + Programmer.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_OID_NAME_STR"></a><a id="cert_oid_name_str"></a><dl>
<dt><b>CERT_OID_NAME_STR</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
OIDs are included with an  equal sign (=) separator from their attribute value. <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn">CERT_RDN</a> entries are separated by a comma followed by a space (, ). Multiple attributes in a <b>CERT_RDN</b> are separated by a plus sign followed by a space (+ ).

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_X500_NAME_STR"></a><a id="cert_x500_name_str"></a><dl>
<dt><b>CERT_X500_NAME_STR</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
OIDs are converted to their <a href="/windows/desktop/SecGloss/x-gly">X.500</a> key names; otherwise, they are the same as <b>CERT_OID_NAME_STR</b>. If an OID does not have a corresponding X.500 name, the OID is used with a prefix of OID. 


 

The RDN value is quoted if it contains leading or trailing white space or one of the following characters:

<ul>
<li>Comma (,)</li>
<li>Plus sign (+)</li>
<li>Equal sign (=)</li>
<li>Inch mark (")</li>
<li>Backslash followed by the letter n (\n)</li>
<li>Less than sign (&lt;)</li>
<li>Greater than sign (&gt;)</li>
<li>Number sign (#)</li>
<li>Semicolon (;)</li>
</ul>
The quotation character is an inch mark ("). If the RDN value contains an inch mark, it is enclosed within quotation marks ("").

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
<td width="40%"><a id="CERT_NAME_STR_SEMICOLON_FLAG"></a><a id="cert_name_str_semicolon_flag"></a><dl>
<dt><b>CERT_NAME_STR_SEMICOLON_FLAG</b></dt>
<dt>0x40000000</dt>
</dl>
</td>
<td width="60%">
Replace the comma followed by a space (, ) separator with a semicolon followed by a space (; ) separator.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_CRLF_FLAG"></a><a id="cert_name_str_crlf_flag"></a><dl>
<dt><b>CERT_NAME_STR_CRLF_FLAG</b></dt>
<dt>0x08000000</dt>
</dl>
</td>
<td width="60%">
Replace the comma followed by a space (, ) separator with a backslash followed by the letter r followed by a backslash followed by the letter n (\r\n) separator.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_NO_PLUS_FLAG"></a><a id="cert_name_str_no_plus_flag"></a><dl>
<dt><b>CERT_NAME_STR_NO_PLUS_FLAG</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
Replace the plus sign enclosed within spaces ( + ) separator with a single space separator.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_NO_QUOTING_FLAG"></a><a id="cert_name_str_no_quoting_flag"></a><dl>
<dt><b>CERT_NAME_STR_NO_QUOTING_FLAG</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
Disable quoting.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_REVERSE_FLAG"></a><a id="cert_name_str_reverse_flag"></a><dl>
<dt><b>CERT_NAME_STR_REVERSE_FLAG</b></dt>
<dt>0x02000000</dt>
</dl>
</td>
<td width="60%">
The order of the RDNs in the  distinguished name string is reversed after decoding. This flag is not set by default.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_DISABLE_IE4_UTF8_FLAG"></a><a id="cert_name_str_disable_ie4_utf8_flag"></a><dl>
<dt><b>CERT_NAME_STR_DISABLE_IE4_UTF8_FLAG</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
By default,  a CERT_RDN_T61_STRING X.500 key string is decoded as UTF8. If UTF8 decoding fails, the X.500 key is decoded as an 8 bit character. Use CERT_NAME_STR_DISABLE_IE4_UTF8_FLAG to  skip the initial attempt to decode as UTF8.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_ENABLE_PUNYCODE_FLAG"></a><a id="cert_name_str_enable_punycode_flag"></a><dl>
<dt><b>CERT_NAME_STR_ENABLE_PUNYCODE_FLAG</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
If the name pointed to by the <i>pName</i> parameter contains an email RDN, and the host name portion of the email address contains a Punycode encoded <a href="/windows/desktop/SecCertEnroll/about-ia5string">IA5String</a>, the name is converted to the Unicode equivalent.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
</table>

### -param psz [out]

A pointer to a character buffer that receives the returned string. The size of this buffer is specified in the <i>csz</i> parameter.

### -param csz [in]

The size, in characters, of the <i>psz</i> buffer. The size must include the terminating null character.

## -returns

Returns the number of characters converted, including the terminating null character. 

If <i>psz</i> is <b>NULL</b> or <i>csz</i> is zero, returns the required size of the destination string.

## -remarks

If <i>psz</i> is not <b>NULL</b> and <i>csz</i> is not zero, the returned <i>psz</i> is always a null-terminated string.

We recommend against using multicomponent RDNs (e.g., CN=James+O=Microsoft) to avoid possible ordering problems when decoding occurs. Instead, consider using single valued RDNs (e.g., CN=James, O=Microsoft).  

The string representation follows the distinguished name specifications in <a href="https://www.ietf.org/rfc/rfc1779.txt">RFC 1779</a> except for the deviations described in the following list.

<ul>
<li>Names that contain quotes are enclosed within double quotation marks.</li>
<li>Empty strings are enclosed within double quotation marks.</li>
<li>Strings that contain consecutive spaces are not enclosed within quotation marks.</li>
<li>Relative Distinguished Name (RDN) values of type <b>CERT_RDN_ENCODED_BLOB</b> or <b>CERT_RDN_OCTET_STRING</b> are formatted in hexadecimal.</li>
<li>If an OID does not have a corresponding X.500 name, the “OID” prefix is used before OID.</li>
<li>RDN values are enclosed with double quotation marks (instead of "\") if they contain  leading white space, trailing white space, or one of the following characters:<ul>
<li>Comma (,)</li>
<li>Plus sign (+)</li>
<li>Equal sign (=)</li>
<li>Inch mark (")</li>
<li>Backslash (/)</li>
<li>Less than sign (&lt;)</li>
<li>Greater than sign (&gt;)</li>
<li>Number sign (#)</li>
<li>Semicolon (;)</li>
</ul>
</li>
<li>The X.500 key name  for stateOrProvinceName (2.5.4.8) OID is "S". This value is different from the RFC 1779 X.500 key name ("ST").</li>
</ul>
In addition, the following X.500 key names are not mentioned in RFC 1779, but may be returned by this API:

<table>
<tr>
<th>Key</th>
<th>Object identifier string</th>
</tr>
<tr>
<td>
E

</td>
<td>
1.2.840.113549.1.9.1

</td>
</tr>
<tr>
<td>
T

</td>
<td>
2.5.4.12

</td>
</tr>
<tr>
<td>
G

</td>
<td>
2.5.4.42

</td>
</tr>
<tr>
<td>
I

</td>
<td>
2.5.4.43

</td>
</tr>
<tr>
<td>
SN

</td>
<td>
2.5.4.4

</td>
</tr>
</table>
 


#### Examples

For an example that uses this function, see 
 
<a href="/windows/desktop/SecCrypto/example-c-program-converting-names-from-certificates-to-asn1-and-back">Example C Program: Converting Names from Certificates to ASN.1 and Back</a>.

<div class="code"></div>




> [!NOTE]
> The wincrypt.h header defines CertNameToStr as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certrdnvaluetostra">CertRDNValueToStr</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certstrtonamea">CertStrToName</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Conversion Functions</a>
