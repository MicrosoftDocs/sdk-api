---
UID: NF:mfidl.IMFCameraControlDefaults.GetRangeInfo
tech.root: mf
title: IMFCameraControlDefaults::GetRangeInfo
ms.date: 05/06/2022
targetos: Windows
description: Gets information about the accepted range, step value, and default value for a camera control.
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
 - IMFCameraControlDefaults::GetRangeInfo
f1_keywords:
 - IMFCameraControlDefaults::GetRangeInfo
 - mfidl/IMFCameraControlDefaults::GetRangeInfo
dev_langs:
 - c++
helpviewer_keywords:
 - GetRangeInfo
---

## -description

Gets information about the accepted range, step value, and default value for a camera control.

## -parameters

### -param rangeInfo

Receives a pointer to a [MF_CAMERA_CONTROL_RANGE_INFO](ns-mfidl-mf_camera_control_range_info.md) structure representing the range information for the control.

## -returns

An HRESULT including the following:

| Value | Description |
| S_OK | Success |
| MF_E_NOT_FOUND | The control does not support basic range values. |

## -remarks

The legacy [PROPSETID_VIDCAP_VIDEOPROCAMP](/windows-hardware/drivers/stream/propsetid-vidcap-videoprocamp) and [PROPSETID_VIDCAP_CAMERACONTROL](/windows-hardware/drivers/stream/propsetid-vidcap-cameracontrol) control sets provide an allowed range and step value of with which a control can be configured, as well as a default value. For other controls, the caller is responsible for knowing whether the underlying control supports the basic range information.  

## -see-also

