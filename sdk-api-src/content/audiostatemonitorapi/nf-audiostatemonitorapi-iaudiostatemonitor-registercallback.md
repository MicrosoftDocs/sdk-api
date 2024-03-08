---
UID: NF:audiostatemonitorapi.IAudioStateMonitor.RegisterCallback
tech.root: CoreAudio
title: IAudioStateMonitor::RegisterCallback
ms.date: 06/21/2023
targetos: Windows
description: Registers an implementation of AudioStateMonitorCallback that is called when the system changes the sound level of the audio streams being monitored by an IAudioStateMonitor.
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
 - IAudioStateMonitor::RegisterCallback
f1_keywords:
 - IAudioStateMonitor::RegisterCallback
 - audiostatemonitorapi/IAudioStateMonitor::RegisterCallback
dev_langs:
 - c++
helpviewer_keywords:
 - RegisterCallback
---

## -description

Registers an implementation of [AudioStateMonitorCallback](nc-audiostatemonitorapi-audiostatemonitorcallback.md) that is called when the system changes the sound level of the audio streams being monitored by an [IAudioStateMonitor](nn-audiostatemonitorapi-iaudiostatemonitor.md).

## -parameters

### -param callback [in]

A pointer to the **AudioStateMonitorCallback** function implementation.

### -param context [in, optional]

A optional void pointer that points to context information provided by the client in the call to [IAudioStateMonitor::RegisterCallback](nf-audiostatemonitorapi-iaudiostatemonitor-registercallback.md).

### -param registration [out]

An Int64 representing the handle to a registration. Pass this handle to [IAudioStateMonitor::UnregisterCallback](nf-audiostatemonitorapi-iaudiostatemonitor-unregistercallback.md) to unregister the callback.

## -returns

Returns an HRESULT including the following values.

| Value | Description |
|-------|-------------|
| S_OK  | Success.    |

## -remarks

## -see-also

