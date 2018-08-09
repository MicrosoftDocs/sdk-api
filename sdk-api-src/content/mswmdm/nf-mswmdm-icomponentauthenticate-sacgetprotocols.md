---
UID: NF:mswmdm.IComponentAuthenticate.SACGetProtocols
title: IComponentAuthenticate::SACGetProtocols
author: windows-sdk-content
description: The SACGetProtocols method is used by a component to discover the authentication protocols supported by another component.
old-location: wmdm\icomponentauthenticate_sacgetprotocols.htm
old-project: WMDM
ms.assetid: db01f2a4-5cd5-4acc-be17-37b4c9861cc9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IComponentAuthenticate interface [windows Media Device Manager],SACGetProtocols method, IComponentAuthenticate.SACGetProtocols, IComponentAuthenticate::SACGetProtocols, IComponentAuthenticateSACGetProtocols, SACGetProtocols, SACGetProtocols method [windows Media Device Manager], SACGetProtocols method [windows Media Device Manager],IComponentAuthenticate interface, mswmdm/IComponentAuthenticate::SACGetProtocols, wmdm.icomponentauthenticate_sacgetprotocols
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IComponentAuthenticate.SACGetProtocols
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

