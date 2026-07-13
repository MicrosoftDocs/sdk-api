---
UID: NF:mfidl.IMFCameraControlMonitor.AddControlSubscription
tech.root: mf
title: IMFCameraControlMonitor::AddControlSubscription
ms.date: 05/03/2022
targetos: Windows
description: Adds a camera control to the list of controls for which IMFCameraControlNotify::OnChange notifications will be raised.
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
 - IMFCameraControlMonitor::AddControlSubscription
f1_keywords:
 - IMFCameraControlMonitor::AddControlSubscription
 - mfidl/IMFCameraControlMonitor::AddControlSubscription
dev_langs:
 - c++
helpviewer_keywords:
 - AddControlSubscription
---

## -description

Adds a camera control to the list of controls for which [IMFCameraControlNotify::OnChange](nf-mfidl-imfcameracontrolnotify-onchange.md) notifications will be raised.

## -parameters

### -param controlSet

The GUID for the camera control set to which the added control belongs.

### -param id

The ID of the control within the control set.

## -returns

An HRESULT including the following:


| Value | Description |
|-------|-------------|
| S_OK  | Success     |
| MF_E_INVALIDREQUEST | The camera control monitor is in the running or shutdown state. |
| MF_E_INVALIDARG | An invalid value was supplied for *controlSet*. See Remarks for more information. |

## -remarks

Attempting to add or remove subscriptions after calling [Start](nf-mfidl-imfcameracontrolmonitor-start.md) but before calling [Stop](nf-mfidl-imfcameracontrolmonitor-stop.md), or after calling [Shutdown](nf-mfidl-imfcameracontrolmonitor-shutdown.md), will result in an error.

The explicitly supported controls include the properties under [PROPSETID_VIDCAP_VIDEOPROCAMP](/windows-hardware/drivers/stream/propsetid-vidcap-videoprocamp) and [PROPSETID_VIDCAP_CAMERACONTROL](/windows-hardware/drivers/stream/propsetid-vidcap-videoprocamp), and [KSPROPERTYSETID_ExtendedCameraControl](/windows-hardware/drivers/stream/kspropertysetid-extendedcameracontrol). If **AddControlSubscription** is called with KSPROPERTYSETID_ANYCAMERACONTROL as the *controlSet* parameter, then the created subscription will provoke callbacks for any control change, even those outside of the previously listed property sets. 

Specifying a value other than KSPROPERTYSETID_ANYCAMERACONTROL, PROPSETID_VIDCAP_VIDEOPROCAMP, 
PROPSETID_VIDCAP_CAMERACONTROL or KSPROPERTYSETID_ExtendedCameraControl will result in an error.

To see a code example that implements this method, see [IMFCameraControlNotify](nn-mfidl-imfcameracontrolnotify.md).

## -see-also

