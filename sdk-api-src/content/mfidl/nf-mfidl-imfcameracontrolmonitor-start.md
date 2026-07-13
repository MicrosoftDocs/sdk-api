---
UID: NF:mfidl.IMFCameraControlMonitor.Start
tech.root: mf
title: IMFCameraControlMonitor::Start
ms.date: 05/03/2022
targetos: Windows
description: Starts the camera control monitor, raising IMFCameraControlNotify::OnChange events for changes to controls registered with IMFCameraControlMonitor::AddControlSubscription.
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
 - IMFCameraControlMonitor::Start
f1_keywords:
 - IMFCameraControlMonitor::Start
 - mfidl/IMFCameraControlMonitor::Start
dev_langs:
 - c++
helpviewer_keywords:
 - Start
---

## -description

Starts the camera control monitor, raising [IMFCameraControlNotify::OnChange](nf-mfidl-imfcameracontrolnotify-onchange.md) notifications for changes to controls registered with [IMFCameraControlMonitor::AddControlSubscription](nf-mfidl-imfcameracontrolmonitor-addcontrolsubscription.md).

## -returns

An HRESULT including the following:

| Value | Description |
|-------|-------------|
| S_OK  | Success     |
| MF_E_INVALIDREQUEST | The camera control monitor has already been started or has been shut down. |

## -remarks

To see a code example that implements this method, see [IMFCameraControlNotify](nn-mfidl-imfcameracontrolnotify.md).

## -see-also

