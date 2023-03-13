---
UID: NF:mfidl.IMFCameraControlNotify.OnError
tech.root: mf
title: IMFCameraControlNotify::OnError
ms.date: 05/02/2022
targetos: Windows
description: Raised when an unrecoverable error occurs within the associated IMFCameraControlMonitor.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll:
req.header: mfidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib:
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: Windows 11 Build 22621
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFCameraControlNotify::OnError
f1_keywords:
 - IMFCameraControlNotify::OnError
 - mfidl/IMFCameraControlNotify::OnError
dev_langs:
 - c++
helpviewer_keywords:
 - OnError
---

## -description

Raised when an unrecoverable error occurs within the associated [IMFCameraControlMonitor](nn-mfidl-imfcameracontrolmonitor.md).

## -parameters

### -param hrStatus

The internal error code associated with the error. Possible error values include the following:

| Value | Description |
|-------|-------------|
| E_OUTOFMEMORY | There were insufficient resources available for the monitor to function properly. |
| MF_INVALID_STATE_ERR | A corruption of memory states has occurred. |

## -remarks

After the call to this function returns, the system will cleanup and remove the reference to the [IMFCameraControlNotify](nn-mfidl-imfcameracontrolnotify.md). Clients do not need to call [IMFCameraControlMonitor::Shutdown](nf-mfidl-imfcameracontrolmonitor-shutdown.md) after receiving an **OnError** notification.

To see a code example that implements this method, see [IMFCameraControlNotify](nn-mfidl-imfcameracontrolnotify.md).

## -see-also

