---
UID: NF:mfidl.IMFCameraControlNotify.OnChange
tech.root: mf
title: IMFCameraControlNotify::OnChange
ms.date: 05/02/2022
targetos: Windows
description: Raised when a camera control value is changed.
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
 - IMFCameraControlNotify::OnChange
f1_keywords:
 - IMFCameraControlNotify::OnChange
 - mfidl/IMFCameraControlNotify::OnChange
dev_langs:
 - c++
helpviewer_keywords:
 - OnChange
---

## -description

Raised when a camera control value is changed.

## -parameters

### -param controlSet

A GUID specifying the camera control set to which the changed control belongs.

### -param id

The ID of the changed control within the control set.

## -remarks

The control for which the **OnChange** event is invoked is specified by calling [IMFCameraControlMonitor::AddControlSubscription](nf-mfidl-imfcameracontrolmonitor-addcontrolsubscription.md). The explicitly supported controls include the properties under [PROPSETID_VIDCAP_VIDEOPROCAMP](/windows-hardware/drivers/stream/propsetid-vidcap-videoprocamp) and [PROPSETID_VIDCAP_CAMERACONTROL](/windows-hardware/drivers/stream/propsetid-vidcap-videoprocamp), and [KSPROPERTYSETID_ExtendedCameraControl](/windows-hardware/drivers/stream/kspropertysetid-extendedcameracontrol). If **AddControlSubscription** is called with KSPROPERTYSETID_ANYCAMERACONTROL as the *controlSet* parameter, then the created subscription will provoke callbacks for any control change, even those outside of the previously listed property sets. If a changed control is outside of those sets, then the **OnChange** callback will have the value KSPROPERTYSETID_ANYCAMERACONTROL as its *controlSet* parameter, but for the explicitly supported property sets, the *controlSet* GUID will still return the supported property set GUID, not KSPROPERTYSETID_ANYCAMERACONTROL. The returned *id* parameter in all cases will be the control ID of the altered control.

To see a code example that implements this method, see [IMFCameraControlNotify](nn-mfidl-imfcameracontrolnotify.md).

## -see-also

