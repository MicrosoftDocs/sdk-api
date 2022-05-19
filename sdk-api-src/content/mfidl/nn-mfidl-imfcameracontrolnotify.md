---
UID: NN:mfidl.IMFCameraControlNotify
tech.root: mf
title: IMFCameraControlNotify
ms.date: 05/02/2022
targetos: Windows
description: Represents the notification callback for changes to camera controls. 
prerelease: true
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: mfidl.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Insider Preview Build 22621
req.target-min-winversvr: Windows Insider Preview Build 22621
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFCameraControlNotify
f1_keywords:
 - IMFCameraControlNotify
 - mfidl/IMFCameraControlNotify
dev_langs:
 - c++
helpviewer_keywords:
 - IMFCameraControlNotify
---

## -description

Represents the notification callback for changes to camera controls. 

## -remarks

Clients implement this interface to receive notifications when another app makes changes to the camera settings for a capture device. Pass the implementation into the [MFCreateCameraControlMonitor](nf-mfidl-mfcreatecameracontrolmonitor.md) function to create an instance of [IMFCameraControlMonitor](nn-mfidl-imfcameracontrolmonitor.md).


## -see-also

