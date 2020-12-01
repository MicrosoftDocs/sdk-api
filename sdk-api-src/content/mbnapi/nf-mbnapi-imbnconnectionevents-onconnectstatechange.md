---
UID: NF:mbnapi.IMbnConnectionEvents.OnConnectStateChange
title: IMbnConnectionEvents::OnConnectStateChange (mbnapi.h)
description: Notification method that indicates whether the connection state of the device has changed.
helpviewer_keywords: ["IMbnConnectionEvents interface [Microsoft Broadband Networks]","OnConnectStateChange method","IMbnConnectionEvents.OnConnectStateChange","IMbnConnectionEvents::OnConnectStateChange","OnConnectStateChange","OnConnectStateChange method [Microsoft Broadband Networks]","OnConnectStateChange method [Microsoft Broadband Networks]","IMbnConnectionEvents interface","mbn.imbnconnectionevents_onconnectstatechange","mbnapi/IMbnConnectionEvents::OnConnectStateChange"]
old-location: mbn\imbnconnectionevents_onconnectstatechange.htm
tech.root: mbn
ms.assetid: 5392e5b7-eac7-40f1-b5cd-adde5a6ff1b8
ms.date: 12/05/2018
ms.keywords: IMbnConnectionEvents interface [Microsoft Broadband Networks],OnConnectStateChange method, IMbnConnectionEvents.OnConnectStateChange, IMbnConnectionEvents::OnConnectStateChange, OnConnectStateChange, OnConnectStateChange method [Microsoft Broadband Networks], OnConnectStateChange method [Microsoft Broadband Networks],IMbnConnectionEvents interface, mbn.imbnconnectionevents_onconnectstatechange, mbnapi/IMbnConnectionEvents::OnConnectStateChange
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
 - IMbnConnectionEvents::OnConnectStateChange
 - mbnapi/IMbnConnectionEvents::OnConnectStateChange
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
 - IMbnConnectionEvents.OnConnectStateChange
---

# IMbnConnectionEvents::OnConnectStateChange


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method that indicates whether the connection state of the device has changed.

## -parameters

### -param newConnection [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> interface that represents the connection on which the state has changed due to a system or network initiated change.

## -returns

This method must return <b>S_OK</b>.

## -remarks

An application can use <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> to get the updated connection state.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionevents">IMbnConnectionEvents</a>