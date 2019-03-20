---
UID: NF:certif.ICertServerPolicy.GetCertificateExtension
title: ICertServerPolicy::GetCertificateExtension (certif.h)
author: windows-sdk-content
description: Retrieves a specific certificate extension.
old-location: security\icertserverpolicy_getcertificateextension.htm
tech.root: SecCrypto
ms.assetid: e2c8e1d5-6ddb-4c8f-8052-f45cd52e2bef
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CCertServerPolicy object [Security],GetCertificateExtension method, GetCertificateExtension, GetCertificateExtension method [Security], GetCertificateExtension method [Security],CCertServerPolicy object, GetCertificateExtension method [Security],ICertServerPolicy interface, ICertServerPolicy interface [Security],GetCertificateExtension method, ICertServerPolicy.GetCertificateExtension, ICertServerPolicy::GetCertificateExtension, PROPTYPE_BINARY, PROPTYPE_DATE, PROPTYPE_LONG, PROPTYPE_STRING, _certsrv_icertserverpolicy_getcertificateextension, certif/ICertServerPolicy::GetCertificateExtension, security.icertserverpolicy_getcertificateextension
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the requested extension value.




## -remarks



The 
<a href="https://msdn.microsoft.com/ba45cda8-49a5-4bd6-af68-90b4b56aff7d">SetContext</a> method must be called prior to calling this method. The call to <b>SetContext</b> specifies which request is used as the current context.

Certificate extensions are distinct from certificate properties. Properties are generic data that is attached to the request. Some of these properties are encoded into the certificate (for example: <i>BeginDate</i>), while others are just used to mark requests in the queue and log. Extensions that are not disabled are encoded into the certificate. Extensions are always marked with an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a>, and always have a critical/noncritical flag.


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




<a href="https://msdn.microsoft.com/7d16161e-9827-46a0-9989-30ebca792bb1">ICertServerPolicy</a>



<a href="https://msdn.microsoft.com/6266e96d-81da-478f-99da-86936b4cfc6b">ICertServerPolicy::GetCertificateExtensionFlags</a>



<a href="https://msdn.microsoft.com/ba45cda8-49a5-4bd6-af68-90b4b56aff7d">ICertServerPolicy::SetContext</a>
 

 

