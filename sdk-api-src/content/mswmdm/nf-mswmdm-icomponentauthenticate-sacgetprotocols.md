---
UID: NF:mswmdm.IComponentAuthenticate.SACGetProtocols
title: IComponentAuthenticate::SACGetProtocols (mswmdm.h)
description: The SACGetProtocols method is used by a component to discover the authentication protocols supported by another component.
helpviewer_keywords: ["IComponentAuthenticate interface [windows Media Device Manager]","SACGetProtocols method","IComponentAuthenticate.SACGetProtocols","IComponentAuthenticate::SACGetProtocols","IComponentAuthenticateSACGetProtocols","SACGetProtocols","SACGetProtocols method [windows Media Device Manager]","SACGetProtocols method [windows Media Device Manager]","IComponentAuthenticate interface","mswmdm/IComponentAuthenticate::SACGetProtocols","wmdm.icomponentauthenticate_sacgetprotocols"]
old-location: wmdm\icomponentauthenticate_sacgetprotocols.htm
tech.root: WMDM
ms.assetid: db01f2a4-5cd5-4acc-be17-37b4c9861cc9
ms.date: 12/05/2018
ms.keywords: IComponentAuthenticate interface [windows Media Device Manager],SACGetProtocols method, IComponentAuthenticate.SACGetProtocols, IComponentAuthenticate::SACGetProtocols, IComponentAuthenticateSACGetProtocols, SACGetProtocols, SACGetProtocols method [windows Media Device Manager], SACGetProtocols method [windows Media Device Manager],IComponentAuthenticate interface, mswmdm/IComponentAuthenticate::SACGetProtocols, wmdm.icomponentauthenticate_sacgetprotocols
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IComponentAuthenticate::SACGetProtocols
 - mswmdm/IComponentAuthenticate::SACGetProtocols
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
 - IComponentAuthenticate.SACGetProtocols
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
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method is implemented by a service provider, and never called by an application.


#### Examples

The following method demonstrates a service provider's implementation of the <b>SACGetProtocols</b> method. It does this by calling <a href="/previous-versions/ms868517(v=msdn.10)">CSecureChannelServer::SACGetProtocols</a> on its private <a href="/windows/desktop/WMDM/csecurechannelserver-class">CSecureChannelServer</a> member.


```cpp

STDMETHODIMP CMyServiceProvider::SACGetProtocols(
    DWORD **ppdwProtocols,
    DWORD  *pdwProtocolCount)
{
    HRESULT hr = E_FAIL;

    // Verify that the global CSecureChannelServer member is valid.
    if(g_pAppSCServer == NULL)
       return hr;

    hr = g_pAppSCServer->SACGetProtocols(
        ppdwProtocols,
        pdwProtocolCount
    );

    return hr;
}

```

## -see-also

<a href="/windows/desktop/WMDM/authenticating-the-service-provider">Authenticating the Service Provider</a>



<a href="/previous-versions/ms868517(v=msdn.10)">CSecureChannelServer::SACGetProtocols</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate">IComponentAuthenticate Interface</a>