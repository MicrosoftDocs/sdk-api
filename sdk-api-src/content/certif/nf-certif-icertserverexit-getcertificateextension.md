---
UID: NF:certif.ICertServerExit.GetCertificateExtension
title: ICertServerExit::GetCertificateExtension (certif.h)
description: Gets a specified certificate extension.
helpviewer_keywords: ["CCertServerExit object [Security]","GetCertificateExtension method","GetCertificateExtension","GetCertificateExtension method [Security]","GetCertificateExtension method [Security]","CCertServerExit object","GetCertificateExtension method [Security]","ICertServerExit interface","ICertServerExit interface [Security]","GetCertificateExtension method","ICertServerExit.GetCertificateExtension","ICertServerExit::GetCertificateExtension","PROPTYPE_BINARY","PROPTYPE_DATE","PROPTYPE_LONG","PROPTYPE_STRING","_certsrv_icertserverexit_getcertificateextension","certif/ICertServerExit::GetCertificateExtension","security.icertserverexit_getcertificateextension"]
old-location: security\icertserverexit_getcertificateextension.htm
tech.root: security
ms.assetid: ba2d2e5f-230e-4e69-8d86-dad9c743e5ee
ms.date: 12/05/2018
ms.keywords: CCertServerExit object [Security],GetCertificateExtension method, GetCertificateExtension, GetCertificateExtension method [Security], GetCertificateExtension method [Security],CCertServerExit object, GetCertificateExtension method [Security],ICertServerExit interface, ICertServerExit interface [Security],GetCertificateExtension method, ICertServerExit.GetCertificateExtension, ICertServerExit::GetCertificateExtension, PROPTYPE_BINARY, PROPTYPE_DATE, PROPTYPE_LONG, PROPTYPE_STRING, _certsrv_icertserverexit_getcertificateextension, certif/ICertServerExit::GetCertificateExtension, security.icertserverexit_getcertificateextension
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
 - ICertServerExit::GetCertificateExtension
 - certif/ICertServerExit::GetCertificateExtension
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
 - ICertServerExit.GetCertificateExtension
 - CCertServerExit.GetCertificateExtension
---

# ICertServerExit::GetCertificateExtension


## -description

The <b>GetCertificateExtension</b> method gets a specified certificate extension.

Note that certificate extensions are distinct from certificate properties. Properties are generic data attached to the request object. Some of these properties are encoded into the certificate (example: <i>BeginDate</i>), while others are just used to mark requests in the queue and log. Extensions that are not disabled are encoded into the certificate. Extensions are always marked with an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> and always have a critical/noncritical flag.

## -parameters

### -param strExtensionName [in]

A string that contains the name of the extension.

### -param Type [in]

Specifies the type of the extension. The type can be one of the following types.

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

A  pointer to a <b>VARIANT</b> that receives the requested extension value.

## -returns

<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and *<i>pvarValue</i> is set to the <b>VARIANT</b> that contains the extension value.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the requested extension value.

## -remarks

You must call 
<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-setcontext">ICertServerExit::SetContext</a> prior to using this method.


#### Examples


```cpp
VARIANT  varExt;
HRESULT  hr;

VariantInit(&varExt);
// Get the Extension value
// bstrExtName is BSTR assigned by EnumerateExtensions.
// pCertServerExit has been used to call SetContext previously.
hr = pCertServerExit->GetCertificateExtension(bstrExtName,
                                              PROPTYPE_BINARY,
                                              &varExt);

if (FAILED(hr))
{
    printf("Failed GetCertificateExtension [%x]\n", hr);
    goto error;
}
// Successful call; Use the value in varExt as needed.
// ...

// When done, clear the Variant
VariantClear(&varExt);
```

## -see-also

<a href="/windows/desktop/api/certif/nn-certif-icertserverexit">ICertServerExit</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-getcertificateextensionflags">ICertServerExit::GetCertificateExtensionFlags</a>



<a href="/windows/desktop/api/certif/nf-certif-icertserverexit-setcontext">ICertServerExit::SetContext</a>