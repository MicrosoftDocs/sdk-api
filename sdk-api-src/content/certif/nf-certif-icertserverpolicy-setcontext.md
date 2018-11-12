---
UID: NF:certif.ICertServerPolicy.SetContext
title: ICertServerPolicy::SetContext
author: windows-sdk-content
description: Specifies the request to be used as the context for subsequent calls to Certificate Services.
old-location: security\icertserverpolicy_setcontext.htm
tech.root: seccrypto
ms.assetid: ba45cda8-49a5-4bd6-af68-90b4b56aff7d
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CCertServerPolicy object [Security],SetContext method, ICertServerPolicy interface [Security],SetContext method, ICertServerPolicy.SetContext, ICertServerPolicy::SetContext, SetContext, SetContext method [Security], SetContext method [Security],CCertServerPolicy object, SetContext method [Security],ICertServerPolicy interface, _certsrv_icertserverpolicy_setcontext, certif/ICertServerPolicy::SetContext, security.icertserverpolicy_setcontext
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
 - ICertServerPolicy.SetContext
 - CCertServerPolicy.SetContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertServerPolicy::SetContext


## -description


The <b>SetContext</b> method specifies the request  to be used as the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">context</a> for subsequent calls to Certificate Services.


## -parameters




### -param Context [in]

Specifies the request. This  parameter must be set to the identical value returned in the  <i>Context</i> parameter of the  
<a href="https://msdn.microsoft.com/en-us/library/Aa385039(v=VS.85).aspx">ICertPolicy::VerifyRequest</a> method.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



The policy module must call the <b>SetContext</b> method first, before calls to any other <a href="https://msdn.microsoft.com/en-us/library/Aa385080(v=VS.85).aspx">ICertServerPolicy</a> method,  so that the interface  references a valid request.


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
hr = pCertServerPolicy-&gt;SetContext( nContext );
if (FAILED(hr))
{
    printf("Failed SetContext [%x]\n", hr);
    goto error;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa385039(v=VS.85).aspx">ICertPolicy::VerifyRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa385080(v=VS.85).aspx">ICertServerPolicy</a>
 

 

