---
UID: NN:mbnapi.IMbnConnection
title: IMbnConnection (mbnapi.h)
description: Represents the network connectivity of a device.
helpviewer_keywords: ["IMbnConnection","IMbnConnection interface [Microsoft Broadband Networks]","IMbnConnection interface [Microsoft Broadband Networks]","described","mbn.imbnconnection","mbnapi/IMbnConnection"]
old-location: mbn\imbnconnection.htm
tech.root: mbn
ms.assetid: dae6ce6f-2534-4799-8ed3-53cd1f2eca13
ms.date: 12/05/2018
ms.keywords: IMbnConnection, IMbnConnection interface [Microsoft Broadband Networks], IMbnConnection interface [Microsoft Broadband Networks],described, mbn.imbnconnection, mbnapi/IMbnConnection
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
 - IMbnConnection
 - mbnapi/IMbnConnection
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
 - IMbnConnection
---

# IMbnConnection interface


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Represents the network connectivity of a device.

## -inheritance

The <b>IMbnConnection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnConnection</b> also has these types of members:

## -remarks

This interface is only available when a Mobile Broadband device is registered to a network or when the device is in <b>MBN_READY_STATE_DEVICE_LOCKED</b> state. When a device deregisters from the network this COM interface is removed and the Mobile Broadband service will call the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionmanagerevents-onconnectionremoval">OnConnectionRemoval</a> method of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionmanagerevents">IMbnConnectionManagerEvents</a> interface.

<b>IMbnConnection</b> objects are provided by calls to the <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionmanager-getconnection">GetConnection</a> and <a href="/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionmanager-getconnections">GetConnections</a> methods of the <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionmanager">IMbnConnectionManager</a> interface.
