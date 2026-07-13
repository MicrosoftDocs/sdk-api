---
UID: NF:mfidl.IMFCameraControlMonitor.Stop
tech.root: mf
title: IMFCameraControlMonitor::Stop
ms.date: 05/03/2022
targetos: Windows
description: Stops the camera control monitor.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: mfsensorgroup.dll
req.header: mfidl.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: mfsensorgroup.lib
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
 - IMFCameraControlMonitor::Stop
f1_keywords:
 - IMFCameraControlMonitor::Stop
 - mfidl/IMFCameraControlMonitor::Stop
dev_langs:
 - c++
helpviewer_keywords:
 - Stop
---

## -description

Stops the camera control monitor.

## -returns

An HRESULT including the following:


| Value | Description |
|-------|-------------|
| S_OK  | Success     |
| MF_E_INVALIDREQUEST | The camera control monitor has already been stopped or has been shut down. |

## -remarks

Stopping the camera control monitor pauses control change notifications through [IMFCameraControlNotify::OnChange](nf-mfidl-imfcameracontrolnotify-onchange.md). While the monitor is stopped, clients can add and remove control subscriptions with calls to [AddControlSubscription](nf-mfidl-imfcameracontrolmonitor-addcontrolsubscription.md) and [RemoveControlSubscription](nf-mfidl-imfcameracontrolmonitor-removecontrolsubscription.md).

To see a code example that implements this method, see [IMFCameraControlNotify](nn-mfidl-imfcameracontrolnotify.md).

## -see-also

