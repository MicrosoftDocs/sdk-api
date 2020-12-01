---
UID: NF:wincrypt.CryptQueryObject
title: CryptQueryObject function (wincrypt.h)
description: Retrieves information about the contents of a cryptography API object, such as a certificate, a certificate revocation list, or a certificate trust list.
helpviewer_keywords: ["CERT_QUERY_CONTENT_CERT","CERT_QUERY_CONTENT_CERT_PAIR","CERT_QUERY_CONTENT_CRL","CERT_QUERY_CONTENT_CTL","CERT_QUERY_CONTENT_FLAG_ALL","CERT_QUERY_CONTENT_FLAG_CERT","CERT_QUERY_CONTENT_FLAG_CERT_PAIR","CERT_QUERY_CONTENT_FLAG_CRL","CERT_QUERY_CONTENT_FLAG_CTL","CERT_QUERY_CONTENT_FLAG_PFX","CERT_QUERY_CONTENT_FLAG_PFX_AND_LOAD","CERT_QUERY_CONTENT_FLAG_PKCS10","CERT_QUERY_CONTENT_FLAG_PKCS7_SIGNED","CERT_QUERY_CONTENT_FLAG_PKCS7_SIGNED_EMBED","CERT_QUERY_CONTENT_FLAG_PKCS7_UNSIGNED","CERT_QUERY_CONTENT_FLAG_SERIALIZED_CERT","CERT_QUERY_CONTENT_FLAG_SERIALIZED_CRL","CERT_QUERY_CONTENT_FLAG_SERIALIZED_CTL","CERT_QUERY_CONTENT_FLAG_SERIALIZED_STORE","CERT_QUERY_CONTENT_PFX","CERT_QUERY_CONTENT_PFX_AND_LOAD","CERT_QUERY_CONTENT_PKCS10","CERT_QUERY_CONTENT_PKCS7_SIGNED","CERT_QUERY_CONTENT_PKCS7_SIGNED_EMBED","CERT_QUERY_CONTENT_PKCS7_UNSIGNED","CERT_QUERY_CONTENT_SERIALIZED_CERT","CERT_QUERY_CONTENT_SERIALIZED_CRL","CERT_QUERY_CONTENT_SERIALIZED_CTL","CERT_QUERY_CONTENT_SERIALIZED_STORE","CERT_QUERY_FORMAT_ASN_ASCII_HEX_ENCODED","CERT_QUERY_FORMAT_BASE64_ENCODED","CERT_QUERY_FORMAT_BINARY","CERT_QUERY_FORMAT_FLAG_ALL","CERT_QUERY_FORMAT_FLAG_ASN_ASCII_HEX_ENCODED","CERT_QUERY_FORMAT_FLAG_BASE64_ENCODED","CERT_QUERY_FORMAT_FLAG_BINARY","CERT_QUERY_OBJECT_BLOB","CERT_QUERY_OBJECT_FILE","CryptQueryObject","CryptQueryObject function [Security]","PKCS_7_ASN_ENCODING","X509_ASN_ENCODING","_crypto2_cryptqueryobject","security.cryptqueryobject","wincrypt/CryptQueryObject"]
old-location: security\cryptqueryobject.htm
tech.root: security
ms.assetid: d882f2b0-0f0a-41c7-afca-a232dc00797b
ms.date: 12/05/2018
ms.keywords: CERT_QUERY_CONTENT_CERT, CERT_QUERY_CONTENT_CERT_PAIR, CERT_QUERY_CONTENT_CRL, CERT_QUERY_CONTENT_CTL, CERT_QUERY_CONTENT_FLAG_ALL, CERT_QUERY_CONTENT_FLAG_CERT, CERT_QUERY_CONTENT_FLAG_CERT_PAIR, CERT_QUERY_CONTENT_FLAG_CRL, CERT_QUERY_CONTENT_FLAG_CTL, CERT_QUERY_CONTENT_FLAG_PFX, CERT_QUERY_CONTENT_FLAG_PFX_AND_LOAD, CERT_QUERY_CONTENT_FLAG_PKCS10, CERT_QUERY_CONTENT_FLAG_PKCS7_SIGNED, CERT_QUERY_CONTENT_FLAG_PKCS7_SIGNED_EMBED, CERT_QUERY_CONTENT_FLAG_PKCS7_UNSIGNED, CERT_QUERY_CONTENT_FLAG_SERIALIZED_CERT, CERT_QUERY_CONTENT_FLAG_SERIALIZED_CRL, CERT_QUERY_CONTENT_FLAG_SERIALIZED_CTL, CERT_QUERY_CONTENT_FLAG_SERIALIZED_STORE, CERT_QUERY_CONTENT_PFX, CERT_QUERY_CONTENT_PFX_AND_LOAD, CERT_QUERY_CONTENT_PKCS10, CERT_QUERY_CONTENT_PKCS7_SIGNED, CERT_QUERY_CONTENT_PKCS7_SIGNED_EMBED, CERT_QUERY_CONTENT_PKCS7_UNSIGNED, CERT_QUERY_CONTENT_SERIALIZED_CERT, CERT_QUERY_CONTENT_SERIALIZED_CRL, CERT_QUERY_CONTENT_SERIALIZED_CTL, CERT_QUERY_CONTENT_SERIALIZED_STORE, CERT_QUERY_FORMAT_ASN_ASCII_HEX_ENCODED, CERT_QUERY_FORMAT_BASE64_ENCODED, CERT_QUERY_FORMAT_BINARY, CERT_QUERY_FORMAT_FLAG_ALL, CERT_QUERY_FORMAT_FLAG_ASN_ASCII_HEX_ENCODED, CERT_QUERY_FORMAT_FLAG_BASE64_ENCODED, CERT_QUERY_FORMAT_FLAG_BINARY, CERT_QUERY_OBJECT_BLOB, CERT_QUERY_OBJECT_FILE, CryptQueryObject, CryptQueryObject function [Security], PKCS_7_ASN_ENCODING, X509_ASN_ENCODING, _crypto2_cryptqueryobject, security.cryptqueryobject, wincrypt/CryptQueryObject
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
 - CryptQueryObject
 - wincrypt/CryptQueryObject
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
 - CryptQueryObject
---

# CryptQueryObject function


## -description

<div class="alert"><b>Important</b>  This API is deprecated. New and existing software should start using <a href="/windows/desktop/SecCNG/cng-portal">Cryptography Next Generation APIs.</a> Microsoft may remove this API in future releases.</div><div> </div>The <b>CryptQueryObject</b> function retrieves information about the contents of a cryptography API object, such as a <a href="/windows/desktop/SecGloss/c-gly">certificate</a>, a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a>, or a <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a>. The object can either reside in a structure in memory or be contained in a file.

## -parameters

### -param dwObjectType [in]

Indicates the type of the object to be queried. This must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_OBJECT_BLOB"></a><a id="cert_query_object_blob"></a><dl>
<dt><b>CERT_QUERY_OBJECT_BLOB</b></dt>
</dl>
</td>
<td width="60%">
The object is stored in a structure in memory.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_OBJECT_FILE"></a><a id="cert_query_object_file"></a><dl>
<dt><b>CERT_QUERY_OBJECT_FILE</b></dt>
</dl>
</td>
<td width="60%">
The object is stored in a file.

</td>
</tr>
</table>

### -param pvObject [in]

A pointer to the object to be queried. 
					The type of data pointer depends on the contents of the <i>dwObjectType</i> parameter.

<table>
<tr>
<th><i>dwObjectType</i> value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_OBJECT_BLOB"></a><a id="cert_query_object_blob"></a><dl>
<dt><b>CERT_QUERY_OBJECT_BLOB</b></dt>
</dl>
</td>
<td width="60%">
This parameter is a pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_BLOB</a>, or similar, structure that contains the object to query.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_OBJECT_FILE"></a><a id="cert_query_object_file"></a><dl>
<dt><b>CERT_QUERY_OBJECT_FILE</b></dt>
</dl>
</td>
<td width="60%">
This parameter is a pointer to a null-terminated Unicode string that contains the path and name of the file to query.

</td>
</tr>
</table>

### -param dwExpectedContentTypeFlags [in]

Indicates the expected content type. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_FLAG_ALL"></a><a id="cert_query_content_flag_all"></a><dl>
<dt><b>CERT_QUERY_CONTENT_FLAG_ALL</b></dt>
</dl>
</td>
<td width="60%">
The content can be any type. This does not include the <b>CERT_QUERY_CONTENT_FLAG_PFX_AND_LOAD</b> flag.

If this flag is specified, this function will attempt to obtain information about the object, trying different content types until the proper content type is found or the content types are exhausted. This is obviously inefficient, so this flag should only be used if the content type is not known.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_FLAG_CERT"></a><a id="cert_query_content_flag_cert"></a><dl>
<dt><b>CERT_QUERY_CONTENT_FLAG_CERT</b></dt>
</dl>
</td>
<td width="60%">
The content is a single certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_FLAG_CERT_PAIR"></a><a id="cert_query_content_flag_cert_pair"></a><dl>
<dt><b>CERT_QUERY_CONTENT_FLAG_CERT_PAIR</b></dt>
</dl>
</td>
<td width="60%">
The content is an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoded X509_CERT_PAIR (an encoded certificate pair that contains either forward, reverse, or forward and reverse cross certificates).

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_FLAG_CRL"></a><a id="cert_query_content_flag_crl"></a><dl>
<dt><b>CERT_QUERY_CONTENT_FLAG_CRL</b></dt>
</dl>
</td>
<td width="60%">
The content is a single CRL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_FLAG_CTL"></a><a id="cert_query_content_flag_ctl"></a><dl>
<dt><b>CERT_QUERY_CONTENT_FLAG_CTL</b></dt>
</dl>
</td>
<td width="60%">
The content is a single CTL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_FLAG_PFX"></a><a id="cert_query_content_flag_pfx"></a><dl>
<dt><b>CERT_QUERY_CONTENT_FLAG_PFX</b></dt>
</dl>
</td>
<td width="60%">
The content is a PFX (<a href="/windows/desktop/SecGloss/p-gly">PKCS #12</a>) packet, but it will not be loaded by this function. You can use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore">PFXImportCertStore</a> function to load this into a store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_FLAG_PFX_AND_LOAD"></a><a id="cert_query_content_flag_pfx_and_load"></a><dl>
<dt><b>CERT_QUERY_CONTENT_FLAG_PFX_AND_LOAD</b></dt>
</dl>
</td>
<td width="60%">
The content is a PFX (<a href="/windows/desktop/SecGloss/p-gly">PKCS #12</a>) packet and will be loaded by this function subject to the conditions specified in the following note.

<div class="alert"><b>Note</b>  <p class="note">If the PFX packet contains an embedded password that is not an empty string or <b>NULL</b>, and the password was not protected to an Active Directory (AD) principal that includes the calling user, this function will not be able to decrypt the PFX packet. The packet can be decrypted, however, if the password used when the PFX packet was created was encrypted to an AD principal and the user, as part of that principal, has permission to decrypt the password. For more information, see the <i>pvPara</i> parameter and the <b>PKCS12_PROTECT_TO_DOMAIN_SIDS</b> flag of the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-pfxexportcertstoreex">PFXExportCertStoreEx</a> function.

<p class="note">You can protect PFX passwords to an AD principal beginning in Windows 8 and Windows Server 2012.

</div>
<div> </div>
<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_FLAG_PKCS7_SIGNED"></a><a id="cert_query_content_flag_pkcs7_signed"></a><dl>
<dt><b>CERT_QUERY_CONTENT_FLAG_PKCS7_SIGNED</b></dt>
</dl>
</td>
<td width="60%">
The content is a PKCS #7 signed
message.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_FLAG_PKCS7_SIGNED_EMBED"></a><a id="cert_query_content_flag_pkcs7_signed_embed"></a><dl>
<dt><b>CERT_QUERY_CONTENT_FLAG_PKCS7_SIGNED_EMBED</b></dt>
</dl>
</td>
<td width="60%">
The content is an embedded PKCS #7
signed message.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_FLAG_PKCS7_UNSIGNED"></a><a id="cert_query_content_flag_pkcs7_unsigned"></a><dl>
<dt><b>CERT_QUERY_CONTENT_FLAG_PKCS7_UNSIGNED</b></dt>
</dl>
</td>
<td width="60%">
The content is a PKCS #7 unsigned
message.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_FLAG_PKCS10"></a><a id="cert_query_content_flag_pkcs10"></a><dl>
<dt><b>CERT_QUERY_CONTENT_FLAG_PKCS10</b></dt>
</dl>
</td>
<td width="60%">
The content is a PKCS #10 message.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_FLAG_SERIALIZED_CERT"></a><a id="cert_query_content_flag_serialized_cert"></a><dl>
<dt><b>CERT_QUERY_CONTENT_FLAG_SERIALIZED_CERT</b></dt>
</dl>
</td>
<td width="60%">
The content is a serialized single
certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_FLAG_SERIALIZED_CRL"></a><a id="cert_query_content_flag_serialized_crl"></a><dl>
<dt><b>CERT_QUERY_CONTENT_FLAG_SERIALIZED_CRL</b></dt>
</dl>
</td>
<td width="60%">
The content is a serialized single CRL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_FLAG_SERIALIZED_CTL"></a><a id="cert_query_content_flag_serialized_ctl"></a><dl>
<dt><b>CERT_QUERY_CONTENT_FLAG_SERIALIZED_CTL</b></dt>
</dl>
</td>
<td width="60%">
The content is serialized single CTL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_FLAG_SERIALIZED_STORE"></a><a id="cert_query_content_flag_serialized_store"></a><dl>
<dt><b>CERT_QUERY_CONTENT_FLAG_SERIALIZED_STORE</b></dt>
</dl>
</td>
<td width="60%">
The content is a serialized store.

</td>
</tr>
</table>

### -param dwExpectedFormatTypeFlags [in]

Indicates the expected format of the returned type. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_FORMAT_FLAG_ALL"></a><a id="cert_query_format_flag_all"></a><dl>
<dt><b>CERT_QUERY_FORMAT_FLAG_ALL</b></dt>
</dl>
</td>
<td width="60%">
The content can be returned in any format.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_FORMAT_FLAG_ASN_ASCII_HEX_ENCODED"></a><a id="cert_query_format_flag_asn_ascii_hex_encoded"></a><dl>
<dt><b>CERT_QUERY_FORMAT_FLAG_ASN_ASCII_HEX_ENCODED</b></dt>
</dl>
</td>
<td width="60%">
The content should be returned in <a href="/windows/desktop/SecGloss/a-gly">ASCII</a> hex-encoded format with a "{ASN}" prefix.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_FORMAT_FLAG_BASE64_ENCODED"></a><a id="cert_query_format_flag_base64_encoded"></a><dl>
<dt><b>CERT_QUERY_FORMAT_FLAG_BASE64_ENCODED</b></dt>
</dl>
</td>
<td width="60%">
The content should be returned in Base64 encoded format.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_FORMAT_FLAG_BINARY"></a><a id="cert_query_format_flag_binary"></a><dl>
<dt><b>CERT_QUERY_FORMAT_FLAG_BINARY</b></dt>
</dl>
</td>
<td width="60%">
The content should be returned in binary format.

</td>
</tr>
</table>

### -param dwFlags [in]

This parameter is reserved for future use and must be set to zero.

### -param pdwMsgAndCertEncodingType [out]

A pointer to a <b>DWORD</b> value that receives the type of encoding used in the message. If this information is not needed, set this parameter to <b>NULL</b>.


This parameter can receives a combination of one or more of the following values.



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

### -param pdwContentType [out]

A pointer to a <b>DWORD</b> value that receives the actual type of the content. If this information is not needed, set this parameter to <b>NULL</b>. The returned content type can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_CERT"></a><a id="cert_query_content_cert"></a><dl>
<dt><b>CERT_QUERY_CONTENT_CERT</b></dt>
</dl>
</td>
<td width="60%">
The content is a single certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_CERT_PAIR"></a><a id="cert_query_content_cert_pair"></a><dl>
<dt><b>CERT_QUERY_CONTENT_CERT_PAIR</b></dt>
</dl>
</td>
<td width="60%">
The content is an ASN.1 encoded X509_CERT_pair.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_CRL"></a><a id="cert_query_content_crl"></a><dl>
<dt><b>CERT_QUERY_CONTENT_CRL</b></dt>
</dl>
</td>
<td width="60%">
The content is a single CRL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_CTL"></a><a id="cert_query_content_ctl"></a><dl>
<dt><b>CERT_QUERY_CONTENT_CTL</b></dt>
</dl>
</td>
<td width="60%">
The content is a single CTL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_PFX"></a><a id="cert_query_content_pfx"></a><dl>
<dt><b>CERT_QUERY_CONTENT_PFX</b></dt>
</dl>
</td>
<td width="60%">
The content is a PFX (<a href="/windows/desktop/SecGloss/p-gly">PKCS #12</a>) packet. This function only verifies that the object is a PKCS #12 packet. The PKCS #12 packet is not loaded into a certificate store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_PFX_AND_LOAD"></a><a id="cert_query_content_pfx_and_load"></a><dl>
<dt><b>CERT_QUERY_CONTENT_PFX_AND_LOAD</b></dt>
</dl>
</td>
<td width="60%">
The content is a PFX (<a href="/windows/desktop/SecGloss/p-gly">PKCS #12</a>) packet, and it has been loaded into a certificate store.

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_PKCS7_SIGNED"></a><a id="cert_query_content_pkcs7_signed"></a><dl>
<dt><b>CERT_QUERY_CONTENT_PKCS7_SIGNED</b></dt>
</dl>
</td>
<td width="60%">
The content is a PKCS #7 signed
message.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_PKCS7_SIGNED_EMBED"></a><a id="cert_query_content_pkcs7_signed_embed"></a><dl>
<dt><b>CERT_QUERY_CONTENT_PKCS7_SIGNED_EMBED</b></dt>
</dl>
</td>
<td width="60%">
The content is an embedded PKCS #7
signed message.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_PKCS7_UNSIGNED"></a><a id="cert_query_content_pkcs7_unsigned"></a><dl>
<dt><b>CERT_QUERY_CONTENT_PKCS7_UNSIGNED</b></dt>
</dl>
</td>
<td width="60%">
The content is a PKCS #7 unsigned
message.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_PKCS10"></a><a id="cert_query_content_pkcs10"></a><dl>
<dt><b>CERT_QUERY_CONTENT_PKCS10</b></dt>
</dl>
</td>
<td width="60%">
The content is a PKCS #10 message.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_SERIALIZED_CERT"></a><a id="cert_query_content_serialized_cert"></a><dl>
<dt><b>CERT_QUERY_CONTENT_SERIALIZED_CERT</b></dt>
</dl>
</td>
<td width="60%">
The content is a serialized single
certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_SERIALIZED_CRL"></a><a id="cert_query_content_serialized_crl"></a><dl>
<dt><b>CERT_QUERY_CONTENT_SERIALIZED_CRL</b></dt>
</dl>
</td>
<td width="60%">
The content is a serialized single CRL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_SERIALIZED_CTL"></a><a id="cert_query_content_serialized_ctl"></a><dl>
<dt><b>CERT_QUERY_CONTENT_SERIALIZED_CTL</b></dt>
</dl>
</td>
<td width="60%">
The content is a serialized single CTL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_SERIALIZED_STORE"></a><a id="cert_query_content_serialized_store"></a><dl>
<dt><b>CERT_QUERY_CONTENT_SERIALIZED_STORE</b></dt>
</dl>
</td>
<td width="60%">
The content is a serialized store.

</td>
</tr>
</table>

### -param pdwFormatType [out]

A pointer to a <b>DWORD</b> value that receives the actual format type of the content. If this information is not needed, set this parameter to <b>NULL</b>. The returned format type can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_FORMAT_ASN_ASCII_HEX_ENCODED"></a><a id="cert_query_format_asn_ascii_hex_encoded"></a><dl>
<dt><b>CERT_QUERY_FORMAT_ASN_ASCII_HEX_ENCODED</b></dt>
</dl>
</td>
<td width="60%">
The content is in <a href="/windows/desktop/SecGloss/a-gly">ASCII</a> hex-encoded format with an "{ASN}" prefix.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_FORMAT_BASE64_ENCODED"></a><a id="cert_query_format_base64_encoded"></a><dl>
<dt><b>CERT_QUERY_FORMAT_BASE64_ENCODED</b></dt>
</dl>
</td>
<td width="60%">
The content is in Base64 encoded format.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_FORMAT_BINARY"></a><a id="cert_query_format_binary"></a><dl>
<dt><b>CERT_QUERY_FORMAT_BINARY</b></dt>
</dl>
</td>
<td width="60%">
The content is in binary format.

</td>
</tr>
</table>

### -param phCertStore [out]

A pointer to an <b>HCERTSTORE</b> value that receives a handle to a certificate store that includes all of the certificates, CRLs, and CTLs in the object.


This parameter only receives a certificate store handle when the <i>dwContentType</i> parameter receives one of the following values. This parameter receives <b>NULL</b> for all other content types.



<a id="CERT_QUERY_CONTENT_CERT"></a>
<a id="cert_query_content_cert"></a>


#### CERT_QUERY_CONTENT_CERT

<a id="CERT_QUERY_CONTENT_CRL"></a>
<a id="cert_query_content_crl"></a>


#### CERT_QUERY_CONTENT_CRL

<a id="CERT_QUERY_CONTENT_CTL"></a>
<a id="cert_query_content_ctl"></a>


#### CERT_QUERY_CONTENT_CTL

<a id="CERT_QUERY_CONTENT_PFX_AND_LOAD"></a>
<a id="cert_query_content_pfx_and_load"></a>


#### CERT_QUERY_CONTENT_PFX_AND_LOAD

<a id="CERT_QUERY_CONTENT_PKCS7_SIGNED"></a>
<a id="cert_query_content_pkcs7_signed"></a>


#### CERT_QUERY_CONTENT_PKCS7_SIGNED

<a id="CERT_QUERY_CONTENT_PKCS7_SIGNED_EMBED"></a>
<a id="cert_query_content_pkcs7_signed_embed"></a>


#### CERT_QUERY_CONTENT_PKCS7_SIGNED_EMBED

<a id="CERT_QUERY_CONTENT_SERIALIZED_CERT"></a>
<a id="cert_query_content_serialized_cert"></a>


#### CERT_QUERY_CONTENT_SERIALIZED_CERT

<a id="CERT_QUERY_CONTENT_SERIALIZED_CRL"></a>
<a id="cert_query_content_serialized_crl"></a>


#### CERT_QUERY_CONTENT_SERIALIZED_CRL

<a id="CERT_QUERY_CONTENT_SERIALIZED_CTL"></a>
<a id="cert_query_content_serialized_ctl"></a>


#### CERT_QUERY_CONTENT_SERIALIZED_CTL

<a id="CERT_QUERY_CONTENT_SERIALIZED_STORE"></a>
<a id="cert_query_content_serialized_store"></a>


#### CERT_QUERY_CONTENT_SERIALIZED_STORE

When you have finished using the handle, free it by passing the handle to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> function.

If this information is not needed, set this parameter to <b>NULL</b>.

### -param phMsg [out]

A pointer to an <b>HCRYPTMSG</b> value that receives the handle of an opened message.


This parameter only receives a message handle when the <i>dwContentType</i> parameter receives one of the following values. This parameter receives <b>NULL</b> for all other content types.



<a id="CERT_QUERY_CONTENT_PKCS7_SIGNED"></a>
<a id="cert_query_content_pkcs7_signed"></a>


#### CERT_QUERY_CONTENT_PKCS7_SIGNED

<a id="CERT_QUERY_CONTENT_PKCS7_SIGNED_EMBED"></a>
<a id="cert_query_content_pkcs7_signed_embed"></a>


#### CERT_QUERY_CONTENT_PKCS7_SIGNED_EMBED

<a id="CERT_QUERY_CONTENT_PKCS7_UNSIGNED"></a>
<a id="cert_query_content_pkcs7_unsigned"></a>


#### CERT_QUERY_CONTENT_PKCS7_UNSIGNED

When you have finished using the handle, free it by passing the handle to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmsgclose">CryptMsgClose</a> function.

If this information is not needed, set this parameter to <b>NULL</b>.

### -param ppvContext [out]

A pointer to a pointer that receives additional information about the object.


The format of this data depends on the value received by the <i>dwContentType</i> parameter. The following table lists the format of the data for the specified <i>dwContentType</i> value.



<table>
<tr>
<th><i>dwContentType</i> value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_CERT"></a><a id="cert_query_content_cert"></a><dl>
<dt><b>CERT_QUERY_CONTENT_CERT</b></dt>
</dl>
</td>
<td width="60%">
This parameter receives a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure. When you have finished using the structure, free it by passing this pointer to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_CRL"></a><a id="cert_query_content_crl"></a><dl>
<dt><b>CERT_QUERY_CONTENT_CRL</b></dt>
</dl>
</td>
<td width="60%">
This parameter receives a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structure. When you have finished using the structure, free it by passing this pointer to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_CTL"></a><a id="cert_query_content_ctl"></a><dl>
<dt><b>CERT_QUERY_CONTENT_CTL</b></dt>
</dl>
</td>
<td width="60%">
This parameter receives a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure. When you have finished using the structure, free it by passing this pointer to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_SERIALIZED_CERT"></a><a id="cert_query_content_serialized_cert"></a><dl>
<dt><b>CERT_QUERY_CONTENT_SERIALIZED_CERT</b></dt>
</dl>
</td>
<td width="60%">
This parameter receives a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure. When you have finished using the structure, free it by passing this pointer to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_SERIALIZED_CRL"></a><a id="cert_query_content_serialized_crl"></a><dl>
<dt><b>CERT_QUERY_CONTENT_SERIALIZED_CRL</b></dt>
</dl>
</td>
<td width="60%">
This parameter receives a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structure. When you have finished using the structure, free it by passing this pointer to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_QUERY_CONTENT_SERIALIZED_CTL"></a><a id="cert_query_content_serialized_ctl"></a><dl>
<dt><b>CERT_QUERY_CONTENT_SERIALIZED_CTL</b></dt>
</dl>
</td>
<td width="60%">
This parameter receives a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure. When you have finished using the structure, free it by passing this pointer to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a> function.

</td>
</tr>
</table>
 

If this information is not needed, set this parameter to <b>NULL</b>.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Data Management Functions</a>