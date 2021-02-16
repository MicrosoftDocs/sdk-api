---
UID: NF:mbnapi.IMbnConnectionManagerEvents.OnConnectionArrival
title: IMbnConnectionManagerEvents::OnConnectionArrival (mbnapi.h)
description: Notification method that indicates a new connection was added to the system.
helpviewer_keywords: ["IMbnConnectionManagerEvents interface [Microsoft Broadband Networks]","OnConnectionArrival method","IMbnConnectionManagerEvents.OnConnectionArrival","IMbnConnectionManagerEvents::OnConnectionArrival","OnConnectionArrival","OnConnectionArrival method [Microsoft Broadband Networks]","OnConnectionArrival method [Microsoft Broadband Networks]","IMbnConnectionManagerEvents interface","mbn.imbnconnectionmanagerevents_onconnectionarrival","mbnapi/IMbnConnectionManagerEvents::OnConnectionArrival"]
old-location: mbn\imbnconnectionmanagerevents_onconnectionarrival.htm
tech.root: mbn
ms.assetid: 88e48ce0-b2eb-431e-be0f-03b1d22ca61b
ms.date: 12/05/2018
ms.keywords: IMbnConnectionManagerEvents interface [Microsoft Broadband Networks],OnConnectionArrival method, IMbnConnectionManagerEvents.OnConnectionArrival, IMbnConnectionManagerEvents::OnConnectionArrival, OnConnectionArrival, OnConnectionArrival method [Microsoft Broadband Networks], OnConnectionArrival method [Microsoft Broadband Networks],IMbnConnectionManagerEvents interface, mbn.imbnconnectionmanagerevents_onconnectionarrival, mbnapi/IMbnConnectionManagerEvents::OnConnectionArrival
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
 - IMbnConnectionManagerEvents::OnConnectionArrival
 - mbnapi/IMbnConnectionManagerEvents::OnConnectionArrival
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
 - IMbnConnectionManagerEvents.OnConnectionArrival
---

# IMbnConnectionManagerEvents::OnConnectionArrival


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method that indicates a new connection was added to the system.

## -parameters

### -param newConnection [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> interface that represents the device added to the system.

## -returns

This method must return <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionmanagerevents">IMbnConnectionManagerEvents</a>