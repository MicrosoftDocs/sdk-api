---
UID: NF:certif.ICertServerPolicy.GetCertificateExtension
title: ICertServerPolicy::GetCertificateExtension (certif.h)
description: Retrieves a specific certificate extension.
helpviewer_keywords: ["CCertServerPolicy object [Security]","GetCertificateExtension method","GetCertificateExtension","GetCertificateExtension method [Security]","GetCertificateExtension method [Security]","CCertServerPolicy object","GetCertificateExtension method [Security]","ICertServerPolicy interface","ICertServerPolicy interface [Security]","GetCertificateExtension method","ICertServerPolicy.GetCertificateExtension","ICertServerPolicy::GetCertificateExtension","PROPTYPE_BINARY","PROPTYPE_DATE","PROPTYPE_LONG","PROPTYPE_STRING","_certsrv_icertserverpolicy_getcertificateextension","certif/ICertServerPolicy::GetCertificateExtension","security.icertserverpolicy_getcertificateextension"]
old-location: security\icertserverpolicy_getcertificateextension.htm
tech.root: security
ms.assetid: e2c8e1d5-6ddb-4c8f-8052-f45cd52e2bef
ms.date: 12/05/2018
ms.keywords: CCertServerPolicy object [Security],GetCertificateExtension method, GetCertificateExtension, GetCertificateExtension method [Security], GetCertificateExtension method [Security],CCertServerPolicy object, GetCertificateExtension method [Security],ICertServerPolicy interface, ICertServerPolicy interface [Security],GetCertificateExtension method, ICertServerPolicy.GetCertificateExtension, ICertServerPolicy::GetCertificateExtension, PROPTYPE_BINARY, PROPTYPE_DATE, PROPTYPE_LONG, PROPTYPE_STRING, _certsrv_icertserverpolicy_getcertificateextension, certif/ICertServerPolicy::GetCertificateExtension, security.icertserverpolicy_getcertificateextension
req.header: certif.h
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
 - ICertServerPolicy::GetCertificateExtension
 - certif/ICertServerPolicy::GetCertificateExtension
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
 - ICertServerPolicy.GetCertificateExtension
 - CCertServerPolicy.GetCertificateExtension
---

# ICertServerPolicy::GetCertificateExtension


## -description

The <b>GetCertificateExtension</b> method retrieves a specific certificate extension.

## -parameters

### -param strExtensionName [in]

A string that contains the name of the extension.

### -param Type [in]

Specifies the type of the extension. The type can be one of the following values.

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
Date/time

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_BINARY"></a><a id="proptype_binary"></a><dl>
<dt><b>PROPTYPE_BINARY</b></dt>
</dl>
</td>
<td width="60%">
The extension value is retrieved as is and is ASN.1 encoded if necessary.

</td>
</tr>
<tr>
<td width="40%"><a id="PROPTYPE_STRING"></a><a id="proptype_string"></a><dl>
<dt><b>PROPTYPE_STRING</b></dt>
</dl>
</td>
<td width="60%">
The extension value is ASN.1 encoded as an IA5 string.

</td>
</tr>
</table>

### -param pvarValue [out]

A pointer to a <b>VARIANT</b> that receives the requested extension value.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and the <i>pvarValue</i> parameter contains the extension value.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the requested extension value.

## -remarks

The 
<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcontext">SetContext</a> method must be called prior to calling this method. The call to <b>SetContext</b> specifies which request is used as the current context.

Certificate extensions are distinct from certificate properties. Properties are generic data that is attached to the request. Some of these properties are encoded into the certificate (for example: <i>BeginDate</i>), while others are just used to mark requests in the queue and log. Extensions that are not disabled are encoded into the certificate. Extensions are always marked with an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a>, and always have a critical/noncritical flag.


#### Examples


```cpp
VARIANT    varExt;
HRESULT    hr;

VariantInit(&varExt);
// Get the Extension value.
// bstrExtName is BSTR assigned by EnumerateExtensions.
// pCertServerPolicy has been used to call SetContext previously.
hr = pCertServerPolicy->GetCertificateExtension(bstrExtName,
                                                PROPTYPE_BINARY,
                                                &varExt);

if (FAILED(hr))
{
    printf("Failed GetCertificateExtension [%x]\n", hr);
    goto error;
}
// Successful call; use the value in varExt as needed.
// ...

// When done, clear the Variant
VariantClear(&varExt);
```

## -see-also

<a href="/windows/desktop/api/certif/nn-certif-icertserverpolicy">ICertServerPolicy</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-getcertificateextensionflags">ICertServerPolicy::GetCertificateExtensionFlags</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverpolicy-setcontext">ICertServerPolicy::SetContext</a>