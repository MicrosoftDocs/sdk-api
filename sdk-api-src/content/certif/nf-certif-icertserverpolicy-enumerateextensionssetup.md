---
UID: NF:certif.ICertServerPolicy.EnumerateExtensionsSetup
title: ICertServerPolicy::EnumerateExtensionsSetup
author: windows-sdk-content
description: Initializes the internal enumeration pointer to the first certificate extension associated with the current context.
old-location: security\icertserverpolicy_enumerateextensionssetup.htm
tech.root: seccrypto
ms.assetid: e7ad32a5-d7df-407f-8efe-c9931610c2d2
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CCertServerPolicy object [Security],EnumerateExtensionsSetup method, EnumerateExtensionsSetup, EnumerateExtensionsSetup method [Security], EnumerateExtensionsSetup method [Security],CCertServerPolicy object, EnumerateExtensionsSetup method [Security],ICertServerPolicy interface, ICertServerPolicy interface [Security],EnumerateExtensionsSetup method, ICertServerPolicy.EnumerateExtensionsSetup, ICertServerPolicy::EnumerateExtensionsSetup, _certsrv_icertserverpolicy_enumerateextensionssetup, certif/ICertServerPolicy::EnumerateExtensionsSetup, security.icertserverpolicy_enumerateextensionssetup
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
 - ICertServerPolicy.EnumerateExtensionsSetup
 - CCertServerPolicy.EnumerateExtensionsSetup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertServerPolicy::EnumerateExtensionsSetup


## -description


The <b>EnumerateExtensionsSetup</b> method initializes the internal enumeration pointer to the first certificate extension associated with the current context.


## -parameters




### -param Flags [in]

This parameter is reserved and must be set to zero.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



The 
<a href="https://msdn.microsoft.com/ba45cda8-49a5-4bd6-af68-90b4b56aff7d">SetContext</a> method must be called prior to calling this method. The call to <b>SetContext</b> specifies which request is the current context.

To retrieve the extension, call the <a href="https://msdn.microsoft.com/565ff4d5-0d22-466d-8458-f98b992a1868">EnumerateExtensions</a> method. The call to <b>EnumerateExtensions</b> retrieves the first extension and moves the index to the next extension if one exists.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Set the context. The value nContext (long) would be the same
// as the context parameter in ICertPolicy::VerifyRequest.
// hr is defined as an HRESULT.
// pCertServerPolicy has been used to call SetContext previously.
hr = pCertServerPolicy-&gt;SetContext( nContext );
if (FAILED(hr))
{
    printf("Failed SetContext [%x]\n", hr);
    goto error;
}
// Setup the enumeration.
hr = pCertServerPolicy-&gt;EnumerateExtensionsSetup( 0 );
if (FAILED(hr))
{
    printf("Failed EnumerateExtensionsSetup [%x]\n", hr);
    goto error;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/565ff4d5-0d22-466d-8458-f98b992a1868">EnumerateExtensions</a>



<a href="https://msdn.microsoft.com/7d16161e-9827-46a0-9989-30ebca792bb1">ICertServerPolicy</a>



<a href="https://msdn.microsoft.com/ba45cda8-49a5-4bd6-af68-90b4b56aff7d">SetContext</a>
 

 

