---
UID: NF:certenc.ICertEncodeStringArray.Reset
title: ICertEncodeStringArray::Reset (certenc.h)
description: Specifies the size of the string array and the type of strings the array will contain.
helpviewer_keywords: ["CCertEncodeStringArray object [Security]","Reset method","CERT_RDN_ANY_TYPE","CERT_RDN_GENERAL_STRING","CERT_RDN_GRAPHIC_STRING","CERT_RDN_IA5_STRING","CERT_RDN_INT4_STRING","CERT_RDN_ISO646_STRING","CERT_RDN_NUMERIC_STRING","CERT_RDN_PRINTABLE_STRING","CERT_RDN_T61_STRING","CERT_RDN_UNICODE_STRING","CERT_RDN_VIDEOTEX_STRING","ICertEncodeStringArray interface [Security]","Reset method","ICertEncodeStringArray.Reset","ICertEncodeStringArray::Reset","Reset","Reset method [Security]","Reset method [Security]","CCertEncodeStringArray object","Reset method [Security]","ICertEncodeStringArray interface","_certsrv_icertencodestringarray_reset","certenc/ICertEncodeStringArray::Reset","security.icertencodestringarray_reset"]
old-location: security\icertencodestringarray_reset.htm
tech.root: security
ms.assetid: 125524ae-236d-4507-9c00-76a016bf6c62
ms.date: 12/05/2018
ms.keywords: CCertEncodeStringArray object [Security],Reset method, CERT_RDN_ANY_TYPE, CERT_RDN_GENERAL_STRING, CERT_RDN_GRAPHIC_STRING, CERT_RDN_IA5_STRING, CERT_RDN_INT4_STRING, CERT_RDN_ISO646_STRING, CERT_RDN_NUMERIC_STRING, CERT_RDN_PRINTABLE_STRING, CERT_RDN_T61_STRING, CERT_RDN_UNICODE_STRING, CERT_RDN_VIDEOTEX_STRING, ICertEncodeStringArray interface [Security],Reset method, ICertEncodeStringArray.Reset, ICertEncodeStringArray::Reset, Reset, Reset method [Security], Reset method [Security],CCertEncodeStringArray object, Reset method [Security],ICertEncodeStringArray interface, _certsrv_icertencodestringarray_reset, certenc/ICertEncodeStringArray::Reset, security.icertencodestringarray_reset
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
 - ICertEncodeStringArray::Reset
 - certenc/ICertEncodeStringArray::Reset
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
 - ICertEncodeStringArray.Reset
 - CCertEncodeStringArray.Reset
---

# ICertEncodeStringArray::Reset


## -description

The <b>Reset</b> method specifies the size of the string array  and the type of strings the array will contain.The values of all the elements in the string array are set to zero.

You must call this method before calling the <a href="/windows/desktop/api/certenc/nf-certenc-icertencodestringarray-setvalue">ICertEncodeStringArray::SetValue</a> method for the first time.

## -parameters

### -param Count [in]

Specifies the number of elements in the string array.

### -param StringType [in]

Specifies the type of strings that the string array contains. The type must be one of the following values. For more information about RDN types, see the CryptoAPI 2.0 documents.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_ANY_TYPE"></a><a id="cert_rdn_any_type"></a><dl>
<dt><b>CERT_RDN_ANY_TYPE</b></dt>
</dl>
</td>
<td width="60%">
For encoding an X509_UNICODE_NAME name.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_NUMERIC_STRING"></a><a id="cert_rdn_numeric_string"></a><dl>
<dt><b>CERT_RDN_NUMERIC_STRING</b></dt>
</dl>
</td>
<td width="60%">
The characters 0 through 9 and the space character (8 bit).

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_PRINTABLE_STRING"></a><a id="cert_rdn_printable_string"></a><dl>
<dt><b>CERT_RDN_PRINTABLE_STRING</b></dt>
</dl>
</td>
<td width="60%">
Printable characters (8 bit).

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_T61_STRING"></a><a id="cert_rdn_t61_string"></a><dl>
<dt><b>CERT_RDN_T61_STRING</b></dt>
</dl>
</td>
<td width="60%">
T.61 encoded characters (8 bit).

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_VIDEOTEX_STRING"></a><a id="cert_rdn_videotex_string"></a><dl>
<dt><b>CERT_RDN_VIDEOTEX_STRING</b></dt>
</dl>
</td>
<td width="60%">
VIDEOTEX characters.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_IA5_STRING"></a><a id="cert_rdn_ia5_string"></a><dl>
<dt><b>CERT_RDN_IA5_STRING</b></dt>
</dl>
</td>
<td width="60%">
IA5 (ASCII) characters.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_GRAPHIC_STRING"></a><a id="cert_rdn_graphic_string"></a><dl>
<dt><b>CERT_RDN_GRAPHIC_STRING</b></dt>
</dl>
</td>
<td width="60%">
A string of ISO-defined GRAPHIC characters.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_ISO646_STRING"></a><a id="cert_rdn_iso646_string"></a><dl>
<dt><b>CERT_RDN_ISO646_STRING</b></dt>
</dl>
</td>
<td width="60%">
128 character set (8 bit).

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_GENERAL_STRING"></a><a id="cert_rdn_general_string"></a><dl>
<dt><b>CERT_RDN_GENERAL_STRING</b></dt>
</dl>
</td>
<td width="60%">
A string of ISO-defined GENERAL characters.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_INT4_STRING"></a><a id="cert_rdn_int4_string"></a><dl>
<dt><b>CERT_RDN_INT4_STRING</b></dt>
</dl>
</td>
<td width="60%">
An array of INT4 values (32 bit).

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_RDN_UNICODE_STRING"></a><a id="cert_rdn_unicode_string"></a><dl>
<dt><b>CERT_RDN_UNICODE_STRING</b></dt>
</dl>
</td>
<td width="60%">
<a href="/windows/desktop/SecGloss/u-gly">Unicode</a> characters (16 bit).

</td>
</tr>
</table>

## -returns

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenc/nn-certenc-icertencodestringarray">ICertEncodeStringArray</a>