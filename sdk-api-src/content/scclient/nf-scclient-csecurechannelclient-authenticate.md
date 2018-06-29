---
UID: NF:scclient.CSecureChannelClient.Authenticate
title: CSecureChannelClient::Authenticate
author: windows-sdk-content
description: The Authenticate method authenticates communication between components to establish trust.
old-location: wmdm\csecurechannelclient_authenticate.htm
old-project: WMDM
ms.assetid: ce96b39f-13f8-47c8-affd-2094cf25f057
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: Authenticate, Authenticate method [windows Media Device Manager], Authenticate method [windows Media Device Manager],CSecureChannelClient interface, CSecureChannelClient interface [windows Media Device Manager],Authenticate method, CSecureChannelClient.Authenticate, CSecureChannelClient::Authenticate, CSecureChannelClientAuthenticate, scclient/CSecureChannelClient::Authenticate, wmdm.csecurechannelclient_authenticate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: scclient.h
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
req.typenames: TS_SB_SORT_BY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - CSecureChannelClient.Authenticate
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# CSecureChannelClient::Authenticate


## -description



The <b>Authenticate</b> method authenticates communication between components to establish trust. In applications, it is used to establish trust between the application and Windows Media Device Manager. Messages are exchanged and trust established if both the client and server certificates are validated.




## -parameters




### -param dwProtocolID [in]

<b>DWORD</b> specifying the protocol identifier. Currently, the only value accepted is SAC_PROTOCOL_V1, defined in the SDK in ...\inc\sac.h.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.

Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>The dwProtocol parameter is invalid.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>
 




## -remarks



This method specifies which protocol method is to be used. That method is then called. In this version of Windows Media Device Manager, SAC_PROTOCOL_V1 must be used.


<a href="https://msdn.microsoft.com/58e8f428-f9b9-438b-8f92-e901537e1076">CSecureChannelClient::SetCertificate</a> and <a href="https://msdn.microsoft.com/b1af8f10-7bad-4f85-89f1-b983af6d4dc9">CSecureChannelClient::SetInterface</a> must be called before <b>Authenticate</b>.


#### Examples

The following C++ code authenticates the Windows Media Device Manager session and acquires an <a href="https://msdn.microsoft.com/cac68821-42fc-4833-bf2e-eec1768869e6">IWMDeviceManager</a> interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Authenticates the WMDM, and acquires an interface to the top-level object.
HRESULT MyClass::Authenticate()
{
    HRESULT hr;
    CComPtr&lt;IComponentAuthenticate&gt; pAuth;

    // Create the WMDM object and acquire 
    // its authentication interface.
    hr = CoCreateInstance(
        __uuidof(MediaDevMgr),
        NULL,
        CLSCTX_INPROC_SERVER,
        __uuidof(IComponentAuthenticate),
        (void**)&amp;pAuth);

    if (hr != S_OK)
        return hr;

    // Create the secure channel client class needed to authenticate the application.
    // We'll use a global member variable to hold the secure channel client
    // in case we need to handle encryption, decryption, or MAC verification
    // during this session.
    m_pSAC = new CSecureChannelClient;
    if (m_pSAC == NULL)
        return E_FAIL;

    // Send the application's transfer certificate and the associated 
    // private key to the secure channel client.
    hr = m_pSAC-&gt;SetCertificate(
        SAC_CERT_V1,
        (BYTE *)abCert, sizeof(abCert),
        (BYTE *)abPVK,  sizeof(abPVK));
    if (hr != S_OK)
        return hr;
            
    // Send the authentication interface we created to the secure channel 
    // client and try authenticating the application with the V1 protocol.
    m_pSAC-&gt;SetInterface(pAuth);
    hr = m_pSAC-&gt;Authenticate(SAC_PROTOCOL_V1);
    if (hr != S_OK)
        return hr;

    // Authenticated succeeded, so we can use the WMDM.
    // Acquire an interface to the top-level WMDM interface
    // and store it in a global variable.
    hr = pAuth-&gt;QueryInterface(__uuidof(IWMDeviceManager), (void**)&amp;m_IWMDeviceMgr);


    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/011815fa-d55c-4abc-9ec8-55d754827342">Authenticating the Application</a>



<a href="https://msdn.microsoft.com/f02220b8-0d1c-416c-97ea-e5e7455fcbba">CSecureChannelClient Class</a>
 

 

