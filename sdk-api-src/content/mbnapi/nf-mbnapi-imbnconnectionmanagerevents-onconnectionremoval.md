---
UID: NF:mbnapi.IMbnConnectionManagerEvents.OnConnectionRemoval
title: IMbnConnectionManagerEvents::OnConnectionRemoval (mbnapi.h)
description: Notification method that indicates a connection was removed from the system.
helpviewer_keywords: ["IMbnConnectionManagerEvents interface [Microsoft Broadband Networks]","OnConnectionRemoval method","IMbnConnectionManagerEvents.OnConnectionRemoval","IMbnConnectionManagerEvents::OnConnectionRemoval","OnConnectionRemoval","OnConnectionRemoval method [Microsoft Broadband Networks]","OnConnectionRemoval method [Microsoft Broadband Networks]","IMbnConnectionManagerEvents interface","mbn.imbnconnectionmanagerevents_onconnectionremoval","mbnapi/IMbnConnectionManagerEvents::OnConnectionRemoval"]
old-location: mbn\imbnconnectionmanagerevents_onconnectionremoval.htm
tech.root: mbn
ms.assetid: 020ee1ad-cab5-4a27-b97b-160319d84ac8
ms.date: 12/05/2018
ms.keywords: IMbnConnectionManagerEvents interface [Microsoft Broadband Networks],OnConnectionRemoval method, IMbnConnectionManagerEvents.OnConnectionRemoval, IMbnConnectionManagerEvents::OnConnectionRemoval, OnConnectionRemoval, OnConnectionRemoval method [Microsoft Broadband Networks], OnConnectionRemoval method [Microsoft Broadband Networks],IMbnConnectionManagerEvents interface, mbn.imbnconnectionmanagerevents_onconnectionremoval, mbnapi/IMbnConnectionManagerEvents::OnConnectionRemoval
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
 - IMbnConnectionManagerEvents::OnConnectionRemoval
 - mbnapi/IMbnConnectionManagerEvents::OnConnectionRemoval
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
 - IMbnConnectionManagerEvents.OnConnectionRemoval
---

# IMbnConnectionManagerEvents::OnConnectionRemoval


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method that indicates a connection was removed from the system.

## -parameters

### -param oldConnection [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> interface that represents the device removed from the system.

## -returns

This method must return <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionmanagerevents">IMbnConnectionManagerEvents</a>