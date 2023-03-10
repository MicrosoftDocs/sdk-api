---
UID: NF:mbnapi.IMbnConnectionEvents.OnDisconnectComplete
title: IMbnConnectionEvents::OnDisconnectComplete (mbnapi.h)
description: Notification method that indicates that a disconnection operation has been performed.
helpviewer_keywords: ["IMbnConnectionEvents interface [Microsoft Broadband Networks]","OnDisconnectComplete method","IMbnConnectionEvents.OnDisconnectComplete","IMbnConnectionEvents::OnDisconnectComplete","OnDisconnectComplete","OnDisconnectComplete method [Microsoft Broadband Networks]","OnDisconnectComplete method [Microsoft Broadband Networks]","IMbnConnectionEvents interface","mbn.imbnconnectionevents_ondisconnectcomplete","mbnapi/IMbnConnectionEvents::OnDisconnectComplete"]
old-location: mbn\imbnconnectionevents_ondisconnectcomplete.htm
tech.root: mbn
ms.assetid: 2d225823-2b9b-4c3a-b847-7b2b9a13d121
ms.date: 12/05/2018
ms.keywords: IMbnConnectionEvents interface [Microsoft Broadband Networks],OnDisconnectComplete method, IMbnConnectionEvents.OnDisconnectComplete, IMbnConnectionEvents::OnDisconnectComplete, OnDisconnectComplete, OnDisconnectComplete method [Microsoft Broadband Networks], OnDisconnectComplete method [Microsoft Broadband Networks],IMbnConnectionEvents interface, mbn.imbnconnectionevents_ondisconnectcomplete, mbnapi/IMbnConnectionEvents::OnDisconnectComplete
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
 - IMbnConnectionEvents::OnDisconnectComplete
 - mbnapi/IMbnConnectionEvents::OnDisconnectComplete
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
 - IMbnConnectionEvents.OnDisconnectComplete
---

# IMbnConnectionEvents::OnDisconnectComplete


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method that indicates that a disconnection operation has been performed.

## -parameters

### -param newConnection [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> interface that represents the connection that has been disconnected.

### -param requestID [in]

The request ID assigned by the Mobile Broadband service to identify the disconnection operation.

### -param status [in]

The operation completion status.  This can only be <b>S_OK</b>.

## -returns

This method must return <b>S_OK</b>.

## -remarks

An application can use <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> to get the current connection state.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionevents">IMbnConnectionEvents</a>