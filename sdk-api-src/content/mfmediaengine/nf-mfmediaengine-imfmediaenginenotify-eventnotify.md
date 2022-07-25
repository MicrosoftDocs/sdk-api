---
UID: NF:mfmediaengine.IMFMediaEngineNotify.EventNotify
title: IMFMediaEngineNotify::EventNotify (mfmediaengine.h)
description: Notifies the application when a playback event occurs.
helpviewer_keywords: ["EventNotify","EventNotify method [Media Foundation]","EventNotify method [Media Foundation]","IMFMediaEngineNotify interface","IMFMediaEngineNotify interface [Media Foundation]","EventNotify method","IMFMediaEngineNotify.EventNotify","IMFMediaEngineNotify::EventNotify","mf.imfmediaenginenotify_eventnotify","mfmediaengine/IMFMediaEngineNotify::EventNotify"]
old-location: mf\imfmediaenginenotify_eventnotify.htm
tech.root: mf
ms.assetid: F6B9E025-53C4-4459-9EC4-EA228065FAD3
ms.date: 12/05/2018
ms.keywords: EventNotify, EventNotify method [Media Foundation], EventNotify method [Media Foundation],IMFMediaEngineNotify interface, IMFMediaEngineNotify interface [Media Foundation],EventNotify method, IMFMediaEngineNotify.EventNotify, IMFMediaEngineNotify::EventNotify, mf.imfmediaenginenotify_eventnotify, mfmediaengine/IMFMediaEngineNotify::EventNotify
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMFMediaEngineNotify::EventNotify
 - mfmediaengine/IMFMediaEngineNotify::EventNotify
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineNotify.EventNotify
---

# IMFMediaEngineNotify::EventNotify


## -description

Notifies the application when a playback event occurs.

## -parameters

### -param event [in]

A member of the <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_event">MF_MEDIA_ENGINE_EVENT</a> enumeration that specifies the event.

### -param param1 [in]

The first event parameter. The meaning of this parameter depends on the event code.

### -param param2 [in]

The second event parameter. The meaning of this parameter depends on the event code.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaenginenotify">IMFMediaEngineNotify</a>