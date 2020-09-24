---
UID: NF:mswmdm.IComponentAuthenticate.SACAuth
title: IComponentAuthenticate::SACAuth (mswmdm.h)
description: The SACAuth method establishes a secure authenticated channel between components.
helpviewer_keywords: ["IComponentAuthenticate interface [windows Media Device Manager]","SACAuth method","IComponentAuthenticate.SACAuth","IComponentAuthenticate::SACAuth","IComponentAuthenticateSACAuth","SACAuth","SACAuth method [windows Media Device Manager]","SACAuth method [windows Media Device Manager]","IComponentAuthenticate interface","mswmdm/IComponentAuthenticate::SACAuth","wmdm.icomponentauthenticate_sacauth"]
old-location: wmdm\icomponentauthenticate_sacauth.htm
tech.root: WMDM
ms.assetid: 26cecd09-5f28-47e5-92ec-c2f277be8052
ms.date: 12/05/2018
ms.keywords: IComponentAuthenticate interface [windows Media Device Manager],SACAuth method, IComponentAuthenticate.SACAuth, IComponentAuthenticate::SACAuth, IComponentAuthenticateSACAuth, SACAuth, SACAuth method [windows Media Device Manager], SACAuth method [windows Media Device Manager],IComponentAuthenticate interface, mswmdm/IComponentAuthenticate::SACAuth, wmdm.icomponentauthenticate_sacauth
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
 - IComponentAuthenticate::SACAuth
 - mswmdm/IComponentAuthenticate::SACAuth
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
 - IComponentAuthenticate.SACAuth
---

# IComponentAuthenticate::SACAuth


## -description

The <b>SACAuth</b> method establishes a secure authenticated channel between components.

## -parameters

### -param dwProtocolID [in]

<b>DWORD</b> containing the protocol identifier. For this version of Windows Media Device Manager, always set this parameter to SAC_PROTOCOL_V1.

### -param dwPass [in]

<b>DWORD</b> containing the number of the current communication pass. A pass consists of two messages, one in each direction. SAC_PROTOCOL_V1 is a two-pass protocol, and the passes are numbered 0 and 1.

### -param pbDataIn [in]

Pointer to the input data.

### -param dwDataInLen [in]

<b>DWORD</b> containing the length of the data to which <i>pbDataIn</i> points.

### -param ppbDataOut [out]

Pointer to a pointer to the output data.

### -param pdwDataOutLen [out]

Pointer to a <b>DWORD</b> containing the length of the data to which <i>ppbDataOut</i> points.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method is called only by service providers. It is called one or more times as dictated by the protocol identifier.

The structure of the data in <i>pbDataIn</i> and <i>ppbDataOut</i> is determined by the values of <i>dwProtocolID</i> and <i>dwPass</i>.


#### Examples

The following C++ code demonstrates a service provider's implementation of <b>SACAuth</b>. It calls <a href="/previous-versions/ms868516(v=msdn.10)">CSecureChannelServer::SACAuth</a> on a previously created private <a href="/windows/desktop/WMDM/csecurechannelserver-class">CSecureChannelServer</a> member.


```cpp

HRESULT CMyServiceProvider::SACAuth(
    DWORD   dwProtocolID,
    DWORD   dwPass,
    BYTE   *pbDataIn,
    DWORD   dwDataInLen,
    BYTE  **ppbDataOut,
    DWORD  *pdwDataOutLen)
{
    HRESULT hr = S_OK;

    // Verify that the global CSecureChannelServer member is valid.
    if(g_pAppSCServer == NULL)
        return E_FAIL;

    hr = g_pAppSCServer->SACAuth(
        dwProtocolID,
        dwPass,
        pbDataIn, dwDataInLen,
        ppbDataOut, pdwDataOutLen
    );
    return hr;
}

```

## -see-also

<a href="/windows/desktop/WMDM/authenticating-the-service-provider">Authenticating the Service Provider</a>



<a href="/previous-versions/ms868516(v=msdn.10)">CSecureChannelServer::SACAuth</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate">IComponentAuthenticate Interface</a>