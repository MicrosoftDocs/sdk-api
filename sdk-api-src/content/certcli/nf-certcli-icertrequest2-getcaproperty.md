---
UID: NF:certcli.ICertRequest2.GetCAProperty
title: ICertRequest2::GetCAProperty (certcli.h)
description: Retrieves a property value for the certification authority (CA). (ICertRequest2.GetCAProperty)
helpviewer_keywords: ["CCertRequest object [Security]","GetCAProperty method","CV_OUT_BASE64","CV_OUT_BASE64HEADER","CV_OUT_BASE64REQUESTHEADER","CV_OUT_BASE64X509CRLHEADER","CV_OUT_BINARY","CV_OUT_HEX","CV_OUT_HEXADDR","CV_OUT_HEXASCII","CV_OUT_HEXASCIIADDR","GetCAProperty","GetCAProperty method [Security]","GetCAProperty method [Security]","CCertRequest object","GetCAProperty method [Security]","ICertRequest interface","GetCAProperty method [Security]","ICertRequest2 interface","ICertRequest interface [Security]","GetCAProperty method","ICertRequest2 interface [Security]","GetCAProperty method","ICertRequest2.GetCAProperty","ICertRequest2::GetCAProperty","ICertRequest::GetCAProperty","PROPTYPE_BINARY","PROPTYPE_DATE","PROPTYPE_LONG","PROPTYPE_STRING","_certsrv_icertrequest2_getcaproperty","certcli/ICertRequest2::GetCAProperty","certcli/ICertRequest::GetCAProperty","security.icertrequest2_getcaproperty"]
old-location: security\icertrequest2_getcaproperty.htm
tech.root: security
ms.assetid: 093d657d-2d9c-4973-a71b-5b134cc35034
ms.date: 12/05/2018
ms.keywords: CCertRequest object [Security],GetCAProperty method, CV_OUT_BASE64, CV_OUT_BASE64HEADER, CV_OUT_BASE64REQUESTHEADER, CV_OUT_BASE64X509CRLHEADER, CV_OUT_BINARY, CV_OUT_HEX, CV_OUT_HEXADDR, CV_OUT_HEXASCII, CV_OUT_HEXASCIIADDR, GetCAProperty, GetCAProperty method [Security], GetCAProperty method [Security],CCertRequest object, GetCAProperty method [Security],ICertRequest interface, GetCAProperty method [Security],ICertRequest2 interface, ICertRequest interface [Security],GetCAProperty method, ICertRequest2 interface [Security],GetCAProperty method, ICertRequest2.GetCAProperty, ICertRequest2::GetCAProperty, ICertRequest::GetCAProperty, PROPTYPE_BINARY, PROPTYPE_DATE, PROPTYPE_LONG, PROPTYPE_STRING, _certsrv_icertrequest2_getcaproperty, certcli/ICertRequest2::GetCAProperty, certcli/ICertRequest::GetCAProperty, security.icertrequest2_getcaproperty
req.header: certcli.h
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
req.dll: Certcli.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertRequest2::GetCAProperty
 - certcli/ICertRequest2::GetCAProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertRequest2.GetCAProperty
 - ICertRequest.GetCAProperty
 - CCertRequest.GetCAProperty
---

# ICertRequest2::GetCAProperty


## -description

The <b>GetCAProperty</b> method retrieves a property value for the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA). This method's functionality is identical to <a href="/windows/desktop/api/certadm/nf-certadm-icertadmin2-getcaproperty">ICertAdmin2::GetCAProperty</a>. For information about this method, see <b>ICertAdmin2::GetCAProperty</b>.

## -parameters

### -param strConfig [in]

Represents a valid configuration string for the CA in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the CA, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="/windows/desktop/api/certcli/nn-certcli-icertconfig">ICertConfig</a>.

### -param PropId [in]

Specifies the property identifier. For information about this parameter, see the table in 
<a href="/windows/desktop/api/certadm/nf-certadm-icertadmin2-getcaproperty">ICertAdmin2::GetCAProperty</a>.

### -param PropIndex [in]

If <i>PropId</i> is indexed, the zero-based index to use when retrieving the property value. If <i>PropId</i> is not indexed, this value is ignored.

### -param PropType [in]

Specifies the type of the property, which corresponds to the Type column in the <i>PropId</i> table. The type can be one of the following types.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_LONG"></a><a id="proptype_long"></a><dl>
<dt><b>PROPTYPE_LONG</b></dt>
</dl>
</td>
<td width="60%">
Signed long data

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_DATE"></a><a id="proptype_date"></a><dl>
<dt><b>PROPTYPE_DATE</b></dt>
</dl>
</td>
<td width="60%">
Date/time (reserved for future use)

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_BINARY"></a><a id="proptype_binary"></a><dl>
<dt><b>PROPTYPE_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary data

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_STRING"></a><a id="proptype_string"></a><dl>
<dt><b>PROPTYPE_STRING</b></dt>
</dl>
</td>
<td width="60%">
<a href="/windows/desktop/SecGloss/u-gly">Unicode</a> string data

</td>
</tr>
</table>

### -param Flags [in]

The following flags can be used to specify the format of the returned property value; these flags have meaning only for binary data (such as certificates, certificate chains, or <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a>) and is ignored otherwise.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_BASE64"></a><a id="cv_out_base64"></a><dl>
<dt><b>CV_OUT_BASE64</b></dt>
</dl>
</td>
<td width="60%">
BASE64 without BEGIN/END

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_BASE64HEADER"></a><a id="cv_out_base64header"></a><dl>
<dt><b>CV_OUT_BASE64HEADER</b></dt>
</dl>
</td>
<td width="60%">
BASE64 with BEGIN CERTIFICATE and END CERTIFICATE

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_BASE64REQUESTHEADER"></a><a id="cv_out_base64requestheader"></a><dl>
<dt><b>CV_OUT_BASE64REQUESTHEADER</b></dt>
</dl>
</td>
<td width="60%">
BASE64 with BEGIN NEW CERTIFICATE REQUEST and END NEW CERTIFICATE REQUEST

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_BASE64X509CRLHEADER"></a><a id="cv_out_base64x509crlheader"></a><dl>
<dt><b>CV_OUT_BASE64X509CRLHEADER</b></dt>
</dl>
</td>
<td width="60%">
BASE64 with BEGIN X509 CRL and END X509 CRL

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_BINARY"></a><a id="cv_out_binary"></a><dl>
<dt><b>CV_OUT_BINARY</b></dt>
</dl>
</td>
<td width="60%">
Binary

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_HEX"></a><a id="cv_out_hex"></a><dl>
<dt><b>CV_OUT_HEX</b></dt>
</dl>
</td>
<td width="60%">
Hexadecimal string

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_HEXADDR"></a><a id="cv_out_hexaddr"></a><dl>
<dt><b>CV_OUT_HEXADDR</b></dt>
</dl>
</td>
<td width="60%">
Hexadecimal string with address/offset

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_HEXASCII"></a><a id="cv_out_hexascii"></a><dl>
<dt><b>CV_OUT_HEXASCII</b></dt>
</dl>
</td>
<td width="60%">
Hexadecimal string with ASCII

</td>
</tr>
<tr>
<td width="40%"><a id="CV_OUT_HEXASCIIADDR"></a><a id="cv_out_hexasciiaddr"></a><dl>
<dt><b>CV_OUT_HEXASCIIADDR</b></dt>
</dl>
</td>
<td width="60%">
Hexadecimal string with ASCII and address/offset

</td>
</tr>
</table>

### -param pvarPropertyValue [out, retval]

A pointer to a <b>VARIANT</b> that receives the requested property value.

When you have finished using the <b>VARIANT</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a> function.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
The return value is a <b>Variant</b> that receives the requested property value.

## -see-also

<b>CCertRequest</b>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest">ICertRequest</a>



<a href="/windows/desktop/api/certcli/nn-certcli-icertrequest2">ICertRequest2</a>
