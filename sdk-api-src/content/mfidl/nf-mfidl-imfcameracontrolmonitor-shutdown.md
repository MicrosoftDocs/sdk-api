---
UID: NF:mfidl.IMFCameraControlMonitor.Shutdown
tech.root: mf
title: IMFCameraControlMonitor::Shutdown
ms.date: 05/03/2022
targetos: Windows
description: 
prerelease: true
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
req.target-min-winverclnt: Windows Insider Preview Build 22621
req.target-min-winversvr: Windows Insider Preview Build 22621
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
 - IMFCameraControlMonitor::Shutdown
f1_keywords:
 - IMFCameraControlMonitor::Shutdown
 - mfidl/IMFCameraControlMonitor::Shutdown
dev_langs:
 - c++
helpviewer_keywords:
 - Shutdown
---

## -description

Shuts down the camera control monitor and cleans up associated resources.

## -remarks

Clients are not required to call [Stop](nf-mfidl-imfcameracontrolmonitor-stop.md) before calling **Shutdown**. After calling **Shutdown** subsequent calls to [Start](nf-mfidl-imfcameracontrolmonitor-start.md), [Stop](nf-mfidl-imfcameracontrolmonitor-stop.md), [AddControlSubscription](nf-mfidl-imfcameracontrolmonitor-addcontrolsubscription.md), or [RemoveControlSubscription](nf-mfidl-imfcameracontrolmonitor-addcontrolsubscription.md) will result in an error.

## -see-also

