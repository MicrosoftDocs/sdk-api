---
UID: NF:wincrypt.CertGetNameStringA
title: CertGetNameStringA function (wincrypt.h)
description: Obtains the subject or issuer name from a certificate CERT_CONTEXT structure and converts it to a null-terminated character string. (ANSI)
helpviewer_keywords: ["CERT_NAME_ATTR_TYPE", "CERT_NAME_DISABLE_IE4_UTF8_FLAG", "CERT_NAME_DNS_TYPE", "CERT_NAME_EMAIL_TYPE", "CERT_NAME_FRIENDLY_DISPLAY_TYPE", "CERT_NAME_ISSUER_FLAG", "CERT_NAME_RDN_TYPE", "CERT_NAME_SEARCH_ALL_NAMES_FLAG", "CERT_NAME_SIMPLE_DISPLAY_TYPE", "CERT_NAME_STR_ENABLE_PUNYCODE_FLAG", "CERT_NAME_UPN_TYPE", "CERT_NAME_URL_TYPE", "CertGetNameStringA", "wincrypt/CertGetNameStringA"]
old-location: security\certgetnamestring.htm
tech.root: security
ms.assetid: 300e6345-0be0-48c7-a3a3-174879cf0bbb
ms.date: 12/05/2018
ms.keywords: CERT_NAME_ATTR_TYPE, CERT_NAME_DISABLE_IE4_UTF8_FLAG, CERT_NAME_DNS_TYPE, CERT_NAME_EMAIL_TYPE, CERT_NAME_FRIENDLY_DISPLAY_TYPE, CERT_NAME_ISSUER_FLAG, CERT_NAME_RDN_TYPE, CERT_NAME_SEARCH_ALL_NAMES_FLAG, CERT_NAME_SIMPLE_DISPLAY_TYPE, CERT_NAME_STR_ENABLE_PUNYCODE_FLAG, CERT_NAME_UPN_TYPE, CERT_NAME_URL_TYPE, CertGetNameString, CertGetNameString function [Security], CertGetNameStringA, CertGetNameStringW, _crypto2_certgetnamestring, security.certgetnamestring, wincrypt/CertGetNameString, wincrypt/CertGetNameStringA, wincrypt/CertGetNameStringW
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CertGetNameStringW (Unicode) and CertGetNameStringA (ANSI)
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
 - CertGetNameStringA
 - wincrypt/CertGetNameStringA
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
 - CertGetNameString
 - CertGetNameStringA
 - CertGetNameStringW
---

# CertGetNameStringA function


## -description

The <b>CertGetNameString</b> function obtains the subject or issuer name from a certificate 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure and converts it to a <b>null</b>-terminated character string.

## -parameters

### -param pCertContext [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> certificate context that includes a subject and issuer name to be converted.

### -param dwType [in]

<b>DWORD</b> indicating how the name is to be found and how the output is to be formatted.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_EMAIL_TYPE"></a><a id="cert_name_email_type"></a><dl>
<dt><b>CERT_NAME_EMAIL_TYPE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
If the certificate has a Subject Alternative Name extension or Issuer Alternative Name, uses the first rfc822Name choice. If no rfc822Name choice is found in the extension, uses the Subject Name field for the Email OID. If either rfc822Name or the Email OID is found, uses the string. Otherwise, returns an empty string (returned character count is 1). <i>pvTypePara</i> is not used and is set to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_RDN_TYPE"></a><a id="cert_name_rdn_type"></a><dl>
<dt><b>CERT_NAME_RDN_TYPE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Converts the Subject Name BLOB by calling <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certnametostra">CertNameToStr</a>. <i>pvTypePara</i> points to a <b>DWORD</b> containing the <i>dwStrType</i> passed to <b>CertNameToStr</b>. If the Subject Name field is empty and the certificate has a Subject Alternative Name extension, uses the first directory Name choice from <b>CertNameToStr</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_ATTR_TYPE"></a><a id="cert_name_attr_type"></a><dl>
<dt><b>CERT_NAME_ATTR_TYPE</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
<i>pvTypePara</i> points to an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) specifying the name attribute to be returned. For example, if <i>pvTypePara</i> is szOID_COMMON_NAME, uses the Subject Name member. If the Subject Name member is empty and the certificate has a Subject Alternative Name extension, uses the first directoryName choice.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_SIMPLE_DISPLAY_TYPE"></a><a id="cert_name_simple_display_type"></a><dl>
<dt><b>CERT_NAME_SIMPLE_DISPLAY_TYPE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Iterates through the following list of name attributes and uses the Subject Name or the Subject Alternative Name extension for the first occurrence of: szOID_COMMON_NAME, szOID_ORGANIZATIONAL_UNIT_NAME, szOID_ORGANIZATION_NAME, or szOID_RSA_emailAddr. 




If one of these attributes is not found, uses the Subject Alternative Name extension for a rfc822Name choice. If there is still no match, uses the first attribute.

<i>pvTypePara</i> is not used and is set to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_FRIENDLY_DISPLAY_TYPE"></a><a id="cert_name_friendly_display_type"></a><dl>
<dt><b>CERT_NAME_FRIENDLY_DISPLAY_TYPE</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Checks the certificate for a CERT_FRIENDLY_NAME_PROP_ID property. If the certificate has this property, it is returned. If the certificate does not have the property, the CERT_NAME_SIMPLE_DISPLAY_TYPE is returned.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_DNS_TYPE"></a><a id="cert_name_dns_type"></a><dl>
<dt><b>CERT_NAME_DNS_TYPE</b></dt>
<dt>6</dt>
</dl>
</td>
<td width="60%">
If the certificate has a Subject Alternative Name extension for issuer, Issuer Alternative Name, search for first DNSName choice. 




If the DNSName choice is not found in the extension, search the Subject Name field for the CN OID, "2.5.4.3".

If the DNSName or CN OID is found, return the string. Otherwise, return an empty string.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_URL_TYPE"></a><a id="cert_name_url_type"></a><dl>
<dt><b>CERT_NAME_URL_TYPE</b></dt>
<dt>7</dt>
</dl>
</td>
<td width="60%">
If the certificate has a Subject Alternative Name extension for issuer, Issuer Alternative Name, search for first URL choice. If the URL choice is found, return the string. Otherwise, return an empty string.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_UPN_TYPE"></a><a id="cert_name_upn_type"></a><dl>
<dt><b>CERT_NAME_UPN_TYPE</b></dt>
<dt>8</dt>
</dl>
</td>
<td width="60%">
If the certificate has a Subject Alternative Name extension, search the OtherName choices looking for a pszObjId == szOID_NT_PRINCIPAL_NAME, ("1.3.6.1.4.1.311.20.2.3"). 




If the UPN OID is found, decode the BLOB as a X509_UNICODE_ANY_STRING and return the decoded string. Otherwise, return an empty string.

</td>
</tr>
</table>

### -param dwFlags [in]

Indicates the type of processing needed. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_ISSUER_FLAG"></a><a id="cert_name_issuer_flag"></a><dl>
<dt><b>CERT_NAME_ISSUER_FLAG</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Acquires the issuer's name. If not set, acquires the subject's name.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_DISABLE_IE4_UTF8_FLAG"></a><a id="cert_name_disable_ie4_utf8_flag"></a><dl>
<dt><b>CERT_NAME_DISABLE_IE4_UTF8_FLAG</b></dt>
<dt>0x00010000</dt>
</dl>
</td>
<td width="60%">
Skips the default initial attempt to decode the value as UTF8 and decodes as 8-bit characters.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_SEARCH_ALL_NAMES_FLAG"></a><a id="cert_name_search_all_names_flag"></a><dl>
<dt><b>CERT_NAME_SEARCH_ALL_NAMES_FLAG</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
If the <i>dwType</i> parameter is set to <b>CERT_NAME_DNS_TYPE</b>, all applicable names are returned for the specified DNS value. If there is no DNS name but there is a CN component in the subject, the CN is returned instead. If there is a CN and a DNS name, only the DNS names are returned. This mimics the SSL chain building policy. If you set this flag for a name type other than <b>CERT_NAME_DNS_TYPE</b>, this function returns a null-terminated empty string.

<b>Windows 8 and Windows Server 2012:  </b>Support for this flag begins.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NAME_STR_ENABLE_PUNYCODE_FLAG"></a><a id="cert_name_str_enable_punycode_flag"></a><dl>
<dt><b>CERT_NAME_STR_ENABLE_PUNYCODE_FLAG</b></dt>
<dt>0x00200000</dt>
</dl>
</td>
<td width="60%">
This flag enables decoding of  <a href="/windows/desktop/SecCertEnroll/about-ia5string">IA5String</a> strings to Unicode string values based on the <i>dwType</i> parameter value as defined below:

<ul>
<li>CERT_NAME_EMAIL_TYPE: If the host name portion of the email address contains a Punycode encoded <a href="/windows/desktop/SecCertEnroll/about-ia5string">IA5String</a> component, it is converted to the Unicode equivalent.</li>
<li>CERT_NAME_SIMPLE_DISPLAY_TYPE: If a Subject Name of szOID_RSA_emailAddr or the rfc822Name from the Subject Alternative Name is returned from the certificate, and the host name portion of the email address a contains Punycode encoded <a href="/windows/desktop/SecCertEnroll/about-ia5string">IA5String</a> component, it is converted to the Unicode equivalent.</li>
<li>CERT_NAME_DNS_TYPE: If the certificate has an Issuer Alternative Name, with a DNSName choice, and the host name portion of the email address a contains Punycode encoded <a href="/windows/desktop/SecCertEnroll/about-ia5string">IA5String</a> component, it is converted to the Unicode equivalent.</li>
<li>CERT_NAME_URL_TYPE: The URI is decoded and unescaped. If the server host name of the URI contains a Punycode encoded <a href="/windows/desktop/SecCertEnroll/about-ia5string">IA5String</a> component, the host name string is converted to the Unicode equivalent.</li>
</ul>
<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
</table>

### -param pvTypePara [in]

A pointer to either a <b>DWORD</b> containing the <i>dwStrType</i> or an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) specifying the name attribute. The type pointed to is determined by the value of <i>dwType</i>.

### -param pszNameString [out]

A pointer to an allocated buffer to receive the returned string. If <i>pszNameString</i> is not <b>NULL</b> and <i>cchNameString</i> is not zero, <i>pszNameString</i> is a <b>null</b>-terminated string.

If <b>CERT_NAME_SEARCH_ALL_NAMES_FLAG</b> is specified in the <i>dwFlags</i> parameter and <b>CERT_NAME_DNS_TYPE</b> is set in the <i>dwType</i> parameter, the returned string will contain all of the DNS names that apply. Each string in the output string is null-terminated and the last string will be double null-terminated. If no DNS names are found, a single null-terminated empty string is returned.

### -param cchNameString [in]

Size, in characters, allocated for the returned string. The size must include the terminating <b>NULL</b> character.

## -returns

Returns the number of characters converted, including the terminating zero character. If <i>pszNameString</i> is <b>NULL</b> or <i>cchNameString</i> is zero, returns the required size of the destination string (including the terminating <b>NULL</b> character). If the specified name type is not found, returns a <b>null</b>-terminated empty string with a returned character count of 1.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Conversion Functions</a>

## -remarks

> [!NOTE]
> The wincrypt.h header defines CertGetNameString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
