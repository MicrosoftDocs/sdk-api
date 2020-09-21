---
UID: NF:mbnapi.IMbnRegistrationEvents.OnPacketServiceStateChange
title: IMbnRegistrationEvents::OnPacketServiceStateChange (mbnapi.h)
description: Notification method called by the Mobile Broadband service to indicate a change in the device packet service state.
helpviewer_keywords: ["IMbnRegistrationEvents interface [Microsoft Broadband Networks]","OnPacketServiceStateChange method","IMbnRegistrationEvents.OnPacketServiceStateChange","IMbnRegistrationEvents::OnPacketServiceStateChange","OnPacketServiceStateChange","OnPacketServiceStateChange method [Microsoft Broadband Networks]","OnPacketServiceStateChange method [Microsoft Broadband Networks]","IMbnRegistrationEvents interface","mbn.imbnregistrationevents_onpacketservicestatechange","mbnapi/IMbnRegistrationEvents::OnPacketServiceStateChange"]
old-location: mbn\imbnregistrationevents_onpacketservicestatechange.htm
tech.root: mbn
ms.assetid: 19199009-a4ac-4bf9-adfc-46c06d861485
ms.date: 12/05/2018
ms.keywords: IMbnRegistrationEvents interface [Microsoft Broadband Networks],OnPacketServiceStateChange method, IMbnRegistrationEvents.OnPacketServiceStateChange, IMbnRegistrationEvents::OnPacketServiceStateChange, OnPacketServiceStateChange, OnPacketServiceStateChange method [Microsoft Broadband Networks], OnPacketServiceStateChange method [Microsoft Broadband Networks],IMbnRegistrationEvents interface, mbn.imbnregistrationevents_onpacketservicestatechange, mbnapi/IMbnRegistrationEvents::OnPacketServiceStateChange
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
 - IMbnRegistrationEvents::OnPacketServiceStateChange
 - mbnapi/IMbnRegistrationEvents::OnPacketServiceStateChange
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
 - IMbnRegistrationEvents.OnPacketServiceStateChange
---

# IMbnRegistrationEvents::OnPacketServiceStateChange


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method called by the Mobile Broadband service to indicate a change in the device packet service state.

## -parameters

### -param newInterface [in]

Pointer to an <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistration">IMbnRegistration</a> interface that represents the device whose packet service state has changed.

## -returns

This method must return <b>S_OK</b>.

## -remarks

The <b>OnPacketServiceStateChange</b> method is called by the Mobile Broadband service to signal a change in the packet service state of the device. This can occur if	there is a change in the current data class, the available data class, or a packet attach network error.
An application can use the passed <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistration">IMbnRegistration</a> interface to get updated state values.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnregistrationevents">IMbnRegistrationEvents</a>