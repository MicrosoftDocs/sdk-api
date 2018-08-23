---
UID: NF:certif.ICertServerPolicy.EnumerateAttributesClose
title: ICertServerPolicy::EnumerateAttributesClose
author: windows-sdk-content
description: Frees the resources connected with attribute enumeration.
old-location: security\icertserverpolicy_enumerateattributesclose.htm
old-project: SecCrypto
ms.assetid: 91cb8edd-7735-44c5-b2c5-d46fa1e33e41
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CCertServerPolicy object [Security],EnumerateAttributesClose method, EnumerateAttributesClose, EnumerateAttributesClose method [Security], EnumerateAttributesClose method [Security],CCertServerPolicy object, EnumerateAttributesClose method [Security],ICertServerPolicy interface, ICertServerPolicy interface [Security],EnumerateAttributesClose method, ICertServerPolicy.EnumerateAttributesClose, ICertServerPolicy::EnumerateAttributesClose, _certsrv_icertserverpolicy_enumerateattributesclose, certif/ICertServerPolicy::EnumerateAttributesClose, security.icertserverpolicy_enumerateattributesclose
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certif.h
req.include-header: Certsrv.h
req.redist: 
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertServerPolicy.EnumerateAttributesClose
 - CCertServerPolicy.EnumerateAttributesClose
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
---

# ICertServerPolicy::EnumerateAttributesClose


## -description


The <b>EnumerateAttributesClose</b> method frees the resources connected with attribute enumeration.


## -parameters






## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



All policy modules should call the <b>EnumerateAttributesClose</b> method after calling the <a href="https://msdn.microsoft.com/14b81b88-36db-4b01-96e6-eafed22ae02e">EnumerateAttributesSetup</a> and  
<a href="https://msdn.microsoft.com/5db05ed9-ab17-462b-9a76-34458489771a">EnumerateAttributes</a> methods.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Close the enumeration.
// hr is defined as an HRESULT.
hr = pCertServerPolicy-&gt;EnumerateAttributesClose();
if (FAILED(hr))
{
    printf("Failed EnumerateAttributesClose [%x]\n", hr);
    goto error;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7d16161e-9827-46a0-9989-30ebca792bb1">ICertServerPolicy</a>



<a href="https://msdn.microsoft.com/5db05ed9-ab17-462b-9a76-34458489771a">ICertServerPolicy::EnumerateAttributes</a>



<a href="https://msdn.microsoft.com/14b81b88-36db-4b01-96e6-eafed22ae02e">ICertServerPolicy::EnumerateAttributesSetup</a>
 

 

