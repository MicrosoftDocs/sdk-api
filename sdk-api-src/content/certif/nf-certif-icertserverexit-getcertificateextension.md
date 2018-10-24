---
UID: NF:certif.ICertServerExit.GetCertificateExtension
title: ICertServerExit::GetCertificateExtension
author: windows-sdk-content
description: Gets a specified certificate extension.
old-location: security\icertserverexit_getcertificateextension.htm
tech.root: SecCrypto
ms.assetid: ba2d2e5f-230e-4e69-8d86-dad9c743e5ee
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: CCertServerExit object [Security],GetCertificateExtension method, GetCertificateExtension, GetCertificateExtension method [Security], GetCertificateExtension method [Security],CCertServerExit object, GetCertificateExtension method [Security],ICertServerExit interface, ICertServerExit interface [Security],GetCertificateExtension method, ICertServerExit.GetCertificateExtension, ICertServerExit::GetCertificateExtension, PROPTYPE_BINARY, PROPTYPE_DATE, PROPTYPE_LONG, PROPTYPE_STRING, _certsrv_icertserverexit_getcertificateextension, certif/ICertServerExit::GetCertificateExtension, security.icertserverexit_getcertificateextension
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICertServerExit.GetCertificateExtension
 - CCertServerExit.GetCertificateExtension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertServerExit::GetCertificateExtension


## -description


The <b>GetCertificateExtension</b> method gets a specified certificate extension.

Note that certificate extensions are distinct from certificate properties. Properties are generic data attached to the request object. Some of these properties are encoded into the certificate (example: <i>BeginDate</i>), while others are just used to mark requests in the queue and log. Extensions that are not disabled are encoded into the certificate. Extensions are always marked with an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> and always have a critical/noncritical flag.


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

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is the requested extension value.




## -remarks



You must call 
<a href="https://msdn.microsoft.com/8d317114-17bd-4b22-8e37-99db72740538">ICertServerExit::SetContext</a> prior to using this method.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>VARIANT  varExt;
HRESULT  hr;

VariantInit(&amp;varExt);
// Get the Extension value
// bstrExtName is BSTR assigned by EnumerateExtensions.
// pCertServerExit has been used to call SetContext previously.
hr = pCertServerExit-&gt;GetCertificateExtension(bstrExtName,
                                              PROPTYPE_BINARY,
                                              &amp;varExt);

if (FAILED(hr))
{
    printf("Failed GetCertificateExtension [%x]\n", hr);
    goto error;
}
// Successful call; Use the value in varExt as needed.
// ...

// When done, clear the Variant
VariantClear(&amp;varExt);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1554c09c-a7c1-44ad-9821-93c0913212fc">ICertServerExit</a>



<a href="https://msdn.microsoft.com/0eee1d67-116b-4f93-9273-b70d50fa2c5d">ICertServerExit::GetCertificateExtensionFlags</a>



<a href="https://msdn.microsoft.com/8d317114-17bd-4b22-8e37-99db72740538">ICertServerExit::SetContext</a>
 

 

