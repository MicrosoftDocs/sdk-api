---
UID: NF:mfvirtualcamera.IMFVirtualCamera.Remove
tech.root: mf
title: IMFVirtualCamera::Remove
ms.date: 05/17/2021
targetos: Windows
description: Disables and unregisters the virtual camera from the system.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: mfsensorgroup.dll
req.header: mfvirtualcamera.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: mfsensorgroup.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - mfsensorgroup.dll
api_name:
 - IMFVirtualCamera::Remove
f1_keywords:
 - IMFVirtualCamera::Remove
 - mfvirtualcamera/IMFVirtualCamera::Remove
dev_langs:
 - c++
---

## -description

Disables and unregisters the virtual camera from the system.  This is the equivalent to physically removing an external camera and uninstalling the driver.

## -returns

Returns an HRESULT value, including but not limited to the following values:

| Error code | Description |
|------------|-------------|
| S_OK    | Succeeded |
| E_ACCESSDENIED | The virtual camera is a system wide camera and the caller does not have permissions to remove it. |

## -remarks

Applications that create virtual cameras during their lifetime should ensure that their virtual cameras are removed when the application is uninstalled.

Calling **Remove** while the virtual camera is in use will result in those applications receiving a MF_E_VIDEO_RECORDING_DEVICE_INVALIDATED error.

## -see-also

