---
UID: NN:mfidl.IMFCameraControlMonitor
tech.root: mf
title: IMFCameraControlMonitor
ms.date: 05/03/2022
targetos: Windows
description: Represents a camera control monitor that is used to subscribe and unsubscribe to notifications when the state of a camera control changes.
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: Windows 11 Build 22621
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFCameraControlMonitor
f1_keywords:
 - IMFCameraControlMonitor
 - mfidl/IMFCameraControlMonitor
dev_langs:
 - c++
helpviewer_keywords:
 - IMFCameraControlMonitor
---

## -description

Represents a camera control monitor that is used to subscribe and unsubscribe to notifications when the state of a camera control changes.

## -remarks

Get an instance of this interface by calling [MFCreateCameraControlMonitor](nf-mfidl-mfcreatecameracontrolmonitor.md). Clients implement the [IMFCameraControlNotify](nn-mfidl-imfcameracontrolnotify.md) interface to receive notifications.


## -see-also

