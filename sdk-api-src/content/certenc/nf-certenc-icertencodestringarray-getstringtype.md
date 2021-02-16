---
UID: NF:certenc.ICertEncodeStringArray.GetStringType
title: ICertEncodeStringArray::GetStringType (certenc.h)
description: Returns the type of string values that the string array contains.
helpviewer_keywords: ["CCertEncodeStringArray object [Security]","GetStringType method","GetStringType","GetStringType method [Security]","GetStringType method [Security]","CCertEncodeStringArray object","GetStringType method [Security]","ICertEncodeStringArray interface","ICertEncodeStringArray interface [Security]","GetStringType method","ICertEncodeStringArray.GetStringType","ICertEncodeStringArray::GetStringType","_certsrv_icertencodestringarray_getstringtype","certenc/ICertEncodeStringArray::GetStringType","security.icertencodestringarray_getstringtype"]
old-location: security\icertencodestringarray_getstringtype.htm
tech.root: security
ms.assetid: 7020f364-4f92-46b8-a8e8-360d8e0fa051
ms.date: 12/05/2018
ms.keywords: CCertEncodeStringArray object [Security],GetStringType method, GetStringType, GetStringType method [Security], GetStringType method [Security],CCertEncodeStringArray object, GetStringType method [Security],ICertEncodeStringArray interface, ICertEncodeStringArray interface [Security],GetStringType method, ICertEncodeStringArray.GetStringType, ICertEncodeStringArray::GetStringType, _certsrv_icertencodestringarray_getstringtype, certenc/ICertEncodeStringArray::GetStringType, security.icertencodestringarray_getstringtype
req.header: certenc.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertEncodeStringArray::GetStringType
 - certenc/ICertEncodeStringArray::GetStringType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenc.dll
api_name:
 - ICertEncodeStringArray.GetStringType
 - CCertEncodeStringArray.GetStringType
---

# ICertEncodeStringArray::GetStringType


## -description

The <b>GetStringType</b> method returns the type of string values that the string array contains.

## -parameters

### -param pStringType [out]

A pointer to a <b>Long</b> that  represents the string type. For a list of string types, see Remarks.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value indicates the type of strings in the string array. For a list of string types, see Remarks.

## -remarks

The following table lists the types of strings that the string array can  contain. For more information about RDN types, see the CryptoAPI 2.0 documents.

<table>
<tr>
<th>String type</th>
<th>Meaning</th>
</tr>
<tr>
<td>CERT_RDN_ANY_TYPE</td>
<td>For encoding an X509_UNICODE_NAME name.</td>
</tr>
<tr>
<td>CERT_RDN_NUMERIC_STRING</td>
<td>The numerals 0 through 9 and the space character (8 bit).</td>
</tr>
<tr>
<td>CERT_RDN_PRINTABLE_STRING</td>
<td>Printable characters (8 bit).</td>
</tr>
<tr>
<td>CERT_RDN_T61_STRING</td>
<td>T.61 encoded characters (8 bit).</td>
</tr>
<tr>
<td>CERT_RDN_VIDEOTEX_STRING</td>
<td>VIDEOTEX characters.</td>
</tr>
<tr>
<td>CERT_RDN_IA5_STRING</td>
<td>IA5 (ASCII) characters.</td>
</tr>
<tr>
<td>CERT_RDN_GRAPHIC_STRING</td>
<td>A string of ISO-defined GRAPHIC characters.</td>
</tr>
<tr>
<td>CERT_RDN_ISO646_STRING</td>
<td>128 character set (8 bit).</td>
</tr>
<tr>
<td>CERT_RDN_GENERAL_STRING</td>
<td>A string of ISO-defined GENERAL characters.</td>
</tr>
<tr>
<td>CERT_RDN_INT4_STRING</td>
<td>An array of INT4 values (32 bit).</td>
</tr>
<tr>
<td>CERT_RDN_UNICODE_STRING</td>
<td><a href="/windows/desktop/SecGloss/u-gly">Unicode</a> characters (16 bit).</td>
</tr>
</table>
 


#### Examples

For an example that uses the <b>GetStringType</b> method, see the <a href="/windows/desktop/api/certenc/nf-certenc-icertencodestringarray-encode">ICertEncodeStringArray::Encode</a> method.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodestringarray">ICertEncodeStringArray</a>



<a href="/windows/desktop/api/certenc/nf-certenc-icertencodestringarray-reset">ICertEncodeStringArray::Reset</a>