---
UID: NF:scclient.CSecureChannelClient.SetCertificate
title: CSecureChannelClient::SetCertificate (scclient.h)
description: The SetCertificate method specifies the certificate and private key of the secure authenticated channel (SAC) client.
helpviewer_keywords: ["CSecureChannelClient class [windows Media Device Manager]","SetCertificate method","CSecureChannelClient.SetCertificate","CSecureChannelClient::SetCertificate","CSecureChannelClientSetCertificate","SetCertificate","SetCertificate method [windows Media Device Manager]","SetCertificate method [windows Media Device Manager]","CSecureChannelClient class","scclient/CSecureChannelClient::SetCertificate","wmdm.csecurechannelclient_setcertificate"]
old-location: wmdm\csecurechannelclient_setcertificate.htm
tech.root: WMDM
ms.assetid: 58e8f428-f9b9-438b-8f92-e901537e1076
ms.date: 12/05/2018
ms.keywords: CSecureChannelClient class [windows Media Device Manager],SetCertificate method, CSecureChannelClient.SetCertificate, CSecureChannelClient::SetCertificate, CSecureChannelClientSetCertificate, SetCertificate, SetCertificate method [windows Media Device Manager], SetCertificate method [windows Media Device Manager],CSecureChannelClient class, scclient/CSecureChannelClient::SetCertificate, wmdm.csecurechannelclient_setcertificate
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
 - CSecureChannelClient::SetCertificate
 - scclient/CSecureChannelClient::SetCertificate
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
 - CSecureChannelClient.SetCertificate
---

# CSecureChannelClient::SetCertificate


## -description

The <b>SetCertificate</b> method specifies the certificate and private key of the secure authenticated channel (SAC) client.

## -parameters

### -param dwFlags [in]

Specifies the type of certificate being passed to this method. It must be set to SAC_CERT_V1.

### -param pbAppCert [in]

Pointer to the first byte of the certificate of the SAC client.

### -param dwCertLen [in]

<b>DWORD</b> specifying the length of the certificate to which <i>pbAppCert</i> points.

### -param pbAppPVK [in]

Pointer to the first byte of the private key of the SAC client.

### -param dwPVKLen [in]

<b>DWORD</b> specifying the length of the private key to which <i>pbAppPVK</i> points.

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
<td>A parameter is invalid or is a <b>NULL</b> pointer.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>

## -remarks

Call the <b>SetCertificate</b> method immediately after creating the <b>CsecureChannelClient</b> object, as in the following Example Code.

You can specify the following dummy values for <i>pbAppCert</i> and <i>pbAppPVK</i> to allow basic functionality:


```cpp

BYTE abPVK[] = {0x00};
BYTE abCert[] = {0x00};

```


You can request a key and certificate from Microsoft as described in <a href="/windows/desktop/WMDM/tools-for-development">Tools for Development</a>.


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

<a href="/windows/desktop/WMDM/authenticating-the-application">Authenticating the Application</a>



<a href="/windows/desktop/WMDM/csecurechannelclient-class">CSecureChannelClient Class</a>



<a href="/previous-versions/ms868518(v=msdn.10)">CSecureChannelServer::SetCertificate</a>



<a href="/windows/desktop/WMDM/using-secure-authenticated-channels">Using Secure Authenticated Channels</a>