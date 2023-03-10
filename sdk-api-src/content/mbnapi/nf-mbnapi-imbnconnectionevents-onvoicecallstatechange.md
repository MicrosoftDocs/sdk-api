---
UID: NF:mbnapi.IMbnConnectionEvents.OnVoiceCallStateChange
title: IMbnConnectionEvents::OnVoiceCallStateChange (mbnapi.h)
description: Notification method that indicates a change in the voice call state of a device.
helpviewer_keywords: ["IMbnConnectionEvents interface [Microsoft Broadband Networks]","OnVoiceCallStateChange method","IMbnConnectionEvents.OnVoiceCallStateChange","IMbnConnectionEvents::OnVoiceCallStateChange","OnVoiceCallStateChange","OnVoiceCallStateChange method [Microsoft Broadband Networks]","OnVoiceCallStateChange method [Microsoft Broadband Networks]","IMbnConnectionEvents interface","mbn.imbnconnectionevents_onvoicecallstatechange","mbnapi/IMbnConnectionEvents::OnVoiceCallStateChange"]
old-location: mbn\imbnconnectionevents_onvoicecallstatechange.htm
tech.root: mbn
ms.assetid: c4f243b0-e6d5-4afc-85ad-0f88140c3beb
ms.date: 12/05/2018
ms.keywords: IMbnConnectionEvents interface [Microsoft Broadband Networks],OnVoiceCallStateChange method, IMbnConnectionEvents.OnVoiceCallStateChange, IMbnConnectionEvents::OnVoiceCallStateChange, OnVoiceCallStateChange, OnVoiceCallStateChange method [Microsoft Broadband Networks], OnVoiceCallStateChange method [Microsoft Broadband Networks],IMbnConnectionEvents interface, mbn.imbnconnectionevents_onvoicecallstatechange, mbnapi/IMbnConnectionEvents::OnVoiceCallStateChange
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
 - IMbnConnectionEvents::OnVoiceCallStateChange
 - mbnapi/IMbnConnectionEvents::OnVoiceCallStateChange
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
 - IMbnConnectionEvents.OnVoiceCallStateChange
---

# IMbnConnectionEvents::OnVoiceCallStateChange


## -description

> [!IMPORTANT]
> Starting in Windows 10, version 1803, the Win32 APIs described in this section are replaced by the Windows Runtime APIs in the [Windows.Networking.Connectivity](/uwp/api/windows.networking.connectivity) namespace.

Notification method that indicates a change in the voice call state of a device.

## -parameters

### -param newConnection [in]

An <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> interface that represents the connection for which the voice call state has changed.

## -returns

This method must return <b>S_OK</b>.

## -remarks

<b>OnVoiceCallStateChange</b> is called when voice call state is available or when there is a change in the voice call state.   An application can use <a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnection">IMbnConnection</a> to get the updated voice call state.

## -see-also

<a href="/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionevents">IMbnConnectionEvents</a>