---
UID: NF:audiostatemonitorapi.IAudioStateMonitor.UnregisterCallback
tech.root: CoreAudio
title: IAudioStateMonitor::UnregisterCallback
ms.date: 06/21/2023
targetos: Windows
description: Unregisters an AudioStateMonitorCallback previously registered with a call to IAudioStateMonitor::RegisterCallback.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: audiostatemonitorapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows build 19043
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - audiostatemonitorapi.h
api_name:
 - IAudioStateMonitor::UnregisterCallback
f1_keywords:
 - IAudioStateMonitor::UnregisterCallback
 - audiostatemonitorapi/IAudioStateMonitor::UnregisterCallback
dev_langs:
 - c++
helpviewer_keywords:
 - UnregisterCallback
---

## -description

Unregisters an [AudioStateMonitorCallback](nc-audiostatemonitorapi-audiostatemonitorcallback.md) previously registered with a call to [IAudioStateMonitor::RegisterCallback](nf-audiostatemonitorapi-iaudiostatemonitor-registercallback.md).

## -parameters

### -param registration

The registration handle obtained from the *registration* output parameter to **RegisterCallback**.

## -remarks

If any callbacks are in progress, this method will block until the callbacks have completed. This method may be called from within the callback, and in this case it will not block.

## -see-also

