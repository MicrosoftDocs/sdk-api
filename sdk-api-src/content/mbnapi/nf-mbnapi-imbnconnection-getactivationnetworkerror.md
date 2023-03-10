---
UID: NF:mbnapi.IMbnConnection.GetActivationNetworkError
title: IMbnConnection::GetActivationNetworkError (mbnapi.h)
description: Gets the network error returned in a Packet Data Protocol (PDP) context activation failure.
helpviewer_keywords: ["GetActivationNetworkError","GetActivationNetworkError method [Microsoft Broadband Networks]","GetActivationNetworkError method [Microsoft Broadband Networks]","IMbnConnection interface","IMbnConnection interface [Microsoft Broadband Networks]","GetActivationNetworkError method","IMbnConnection.GetActivationNetworkError","IMbnConnection::GetActivationNetworkError","mbn.imbnconnection_getactivationnetworkerror","mbnapi/IMbnConnection::GetActivationNetworkError"]
old-location: mbn\imbnconnection_getactivationnetworkerror.htm
tech.root: mbn
ms.assetid: a8bda00b-5eff-46a4-b640-1794e8ea21cf
ms.date: 12/05/2018
ms.keywords: GetActivationNetworkError, GetActivationNetworkError method [Microsoft Broadband Networks], GetActivationNetworkError method [Microsoft Broadband Networks],IMbnConnection interface, IMbnConnection interface [Microsoft Broadband Networks],GetActivationNetworkError method, IMbnConnection.GetActivationNetworkError, IMbnConnection::GetActivationNetworkError, mbn.imbnconnection_getactivationnetworkerror, mbnapi/IMbnConnection::GetActivationNetworkError
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMbnConnection::GetActivationNetworkError
 - mbnapi/IMbnConnection::GetActivationNetworkError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnConnection.GetActivationNetworkError
---

# IMbnConnection::GetActivationNetworkError


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Gets the network error returned in a Packet Data Protocol (PDP) context activation failure.

## -parameters

### -param networkError [out, retval]

The error code returned by the network from the last connection context activation operation.  The value is meaningful only if the method returns <b>S_OK</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For GSM devices these error codes are defined in 3GPP specification 24.008 as cause codes. For CDMA devices, device and network specific error codes are used.

The error codes are cleared when the context activation operation completes successfully. When there is no network error or the error is not known, then the value is set to 0.

Whenever there is a change in the network error value, the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionevents-onconnectstatechange">OnConnectStateChange</a> member of <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionevents">IMbnConnectionEvents</a>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a>