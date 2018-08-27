---
UID: NF:scclient.CSecureChannelClient.SetInterface
title: CSecureChannelClient::SetInterface
author: windows-sdk-content
description: The SetInterface method is used by applications to set the IComponentAuthenticate interface to use for Secure Authenticated Channel (SAC) operations.
old-location: wmdm\csecurechannelclient_setinterface.htm
old-project: WMDM
ms.assetid: b1af8f10-7bad-4f85-89f1-b983af6d4dc9
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: CSecureChannelClient interface [windows Media Device Manager],SetInterface method, CSecureChannelClient.SetInterface, CSecureChannelClient::SetInterface, CSecureChannelClientSetInterface, SetInterface, SetInterface method [windows Media Device Manager], SetInterface method [windows Media Device Manager],CSecureChannelClient interface, scclient/CSecureChannelClient::SetInterface, wmdm.csecurechannelclient_setinterface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: scclient.h
req.include-header: 
req.redist: 
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
 - CSecureChannelClient.SetInterface
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# CSecureChannelClient::SetInterface


## -description



The <b>SetInterface</b> method is used by applications to set the <b>IComponentAuthenticate</b> interface to use for Secure Authenticated Channel (SAC) operations.




## -parameters




### -param pComponentAuth [in]

Pointer to an <a href="https://msdn.microsoft.com/5da66dc2-825d-4332-b1cb-2b9d0fabb445">IComponentAuthenticate</a> interface. The caller is responsible for calling <b>Release</b> on the retrieved interface.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/37e4ad70-afe9-40d6-8c4b-e5fcaa8db4ad">Error Codes</a>.

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
<td>The pComponentAuth parameter is invalid or is a <b>NULL</b> pointer.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>
 




## -remarks



The SAC interface is the <b>IComponentAuthenticate</b> interface. Applications use the <b>IComponentAuthenticate</b> interface provided in Windows Media Device Manager. Service providers and secure content providers must implement their own <b>IComponentAuthenticate</b> interface.

<b>CoCreateInstance</b> must be called first to acquire the <b>IComponentAuthenticate</b> interface.


#### Examples

The following C++ code authenticates the Windows Media Device Manager session and acquires the root object.


```cpp

// Authenticates the WMDM, and acquires an interface to the top-level object.
HRESULT MyClass::Authenticate()
{
    HRESULT hr;
    CComPtr<IComponentAuthenticate> pAuth;

    // Create the WMDM object and acquire 
    // its authentication interface.
    hr = CoCreateInstance(
        __uuidof(MediaDevMgr),
        NULL,
        CLSCTX_INPROC_SERVER,
        __uuidof(IComponentAuthenticate),
        (void**)&pAuth);

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
    hr = m_pSAC->SetCertificate(
        SAC_CERT_V1,
        (BYTE *)abCert, sizeof(abCert),
        (BYTE *)abPVK,  sizeof(abPVK));
    if (hr != S_OK)
        return hr;
            
    // Send the authentication interface we created to the secure channel 
    // client and try authenticating the application with the V1 protocol.
    m_pSAC->SetInterface(pAuth);
    hr = m_pSAC->Authenticate(SAC_PROTOCOL_V1);
    if (hr != S_OK)
        return hr;

    // Authenticated succeeded, so we can use the WMDM.
    // Acquire an interface to the top-level WMDM interface.
    hr = pAuth->QueryInterface(__uuidof(IWMDeviceManager), (void**)&m_IWMDeviceMgr);


    return hr;
}

```





## -see-also




<a href="https://msdn.microsoft.com/011815fa-d55c-4abc-9ec8-55d754827342">Authenticating the Application</a>



<a href="https://msdn.microsoft.com/f02220b8-0d1c-416c-97ea-e5e7455fcbba">CSecureChannelClient Class</a>



<a href="https://msdn.microsoft.com/5da66dc2-825d-4332-b1cb-2b9d0fabb445">IComponentAuthenticate Interface</a>



<a href="https://msdn.microsoft.com/ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7">Using Secure Authenticated Channels</a>
 

 

