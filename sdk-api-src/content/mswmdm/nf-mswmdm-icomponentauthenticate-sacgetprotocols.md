---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IComponentAuthenticate::SACGetProtocols


## -description



The <b>SACGetProtocols</b> method is used by a component to discover the authentication protocols supported by another component.




## -parameters




### -param ppdwProtocols [out]

Pointer to an array of supported protocols. For this version of Windows Media Device Manager, it is a single-element <b>DWORD</b> array containing the value SAC_PROTOCOL_V1.


### -param pdwProtocolCount [out]

Pointer to a <b>DWORD</b> containing the number of protocols returned in <i>ppdwProtocols</i>. The number is always 1 for this version.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method is implemented by a service provider, and never called by an application.


#### Examples

The following method demonstrates a service provider's implementation of the <b>SACGetProtocols</b> method. It does this by calling <a href="https://msdn.microsoft.com/42878774-9c8b-4d80-a17e-6682da4d34ab">CSecureChannelServer::SACGetProtocols</a> on its private <a href="https://msdn.microsoft.com/e6e1463a-5a26-4b83-85e0-a639d384a199">CSecureChannelServer</a> member.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
STDMETHODIMP CMyServiceProvider::SACGetProtocols(
    DWORD **ppdwProtocols,
    DWORD  *pdwProtocolCount)
{
    HRESULT hr = E_FAIL;

    // Verify that the global CSecureChannelServer member is valid.
    if(g_pAppSCServer == NULL)
       return hr;

    hr = g_pAppSCServer-&gt;SACGetProtocols(
        ppdwProtocols,
        pdwProtocolCount
    );

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e48a8a7c-0277-4f0c-bad2-5bc9d0286da8">Authenticating the Service Provider</a>



<a href="https://msdn.microsoft.com/42878774-9c8b-4d80-a17e-6682da4d34ab">CSecureChannelServer::SACGetProtocols</a>



<a href="https://msdn.microsoft.com/5da66dc2-825d-4332-b1cb-2b9d0fabb445">IComponentAuthenticate Interface</a>
 

 

