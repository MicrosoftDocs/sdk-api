---
UID: NF:scclient.CSecureChannelClient.Authenticate
title: CSecureChannelClient::Authenticate (scclient.h)
description: The Authenticate method authenticates communication between components to establish trust.
helpviewer_keywords: ["Authenticate","Authenticate method [windows Media Device Manager]","Authenticate method [windows Media Device Manager]","CSecureChannelClient class","CSecureChannelClient class [windows Media Device Manager]","Authenticate method","CSecureChannelClient.Authenticate","CSecureChannelClient::Authenticate","CSecureChannelClientAuthenticate","scclient/CSecureChannelClient::Authenticate","wmdm.csecurechannelclient_authenticate"]
old-location: wmdm\csecurechannelclient_authenticate.htm
tech.root: WMDM
ms.assetid: ce96b39f-13f8-47c8-affd-2094cf25f057
ms.date: 12/05/2018
ms.keywords: Authenticate, Authenticate method [windows Media Device Manager], Authenticate method [windows Media Device Manager],CSecureChannelClient class, CSecureChannelClient class [windows Media Device Manager],Authenticate method, CSecureChannelClient.Authenticate, CSecureChannelClient::Authenticate, CSecureChannelClientAuthenticate, scclient/CSecureChannelClient::Authenticate, wmdm.csecurechannelclient_authenticate
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CSecureChannelClient::Authenticate
 - scclient/CSecureChannelClient::Authenticate
dev_langs:
 - c++
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
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

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


<a href="/previous-versions/ms868504(v=msdn.10)">CSecureChannelClient::SetCertificate</a> and <a href="/previous-versions/bb231595(v=vs.85)">CSecureChannelClient::SetInterface</a> must be called before <b>Authenticate</b>.


#### Examples

The following C++ code authenticates the Windows Media Device Manager session and acquires an <a href="/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager">IWMDeviceManager</a> interface.


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
    // Acquire an interface to the top-level WMDM interface
    // and store it in a global variable.
    hr = pAuth->QueryInterface(__uuidof(IWMDeviceManager), (void**)&m_IWMDeviceMgr);


    return hr;
}

```

## -see-also

<a href="/windows/desktop/WMDM/authenticating-the-application">Authenticating the Application</a>



<a href="/windows/desktop/WMDM/csecurechannelclient-class">CSecureChannelClient Class</a>