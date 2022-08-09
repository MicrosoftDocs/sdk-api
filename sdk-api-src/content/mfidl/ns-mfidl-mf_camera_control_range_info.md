---
UID: NS:mfidl.__MIDL___MIDL_itf_mfidl_0000_0136_0002
tech.root: mf
title: MF_CAMERA_CONTROL_RANGE_INFO
ms.date: 08/05/2022
targetos: Windows
description: The MF_CAMERA_CONTROL_RANGE_INFO structure represents the accepted range, step value, and default value for a camera control.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: mfidl.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: Windows 11 Build 22621
req.target-type: 
req.typenames: MF_CAMERA_CONTROL_RANGE_INFO
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - __MIDL___MIDL_itf_mfidl_0000_0136_0002
 - MF_CAMERA_CONTROL_RANGE_INFO
f1_keywords:
 - __MIDL___MIDL_itf_mfidl_0000_0136_0002
 - mfidl/__MIDL___MIDL_itf_mfidl_0000_0136_0002
 - MF_CAMERA_CONTROL_RANGE_INFO
 - mfidl/MF_CAMERA_CONTROL_RANGE_INFO
dev_langs:
 - c++
helpviewer_keywords:
 - __MIDL___MIDL_itf_mfidl_0000_0136_0002
---

## -description

Represents the accepted range, step value, and default value for a camera control.

## -struct-fields

### -field minValue

The minimum value supported by the control.

### -field maxValue

The maximum value supported by the control.

### -field stepValue

The incremental step value supported by the control.

### -field defaultValue

The default value for the control.

## -remarks

The legacy [PROPSETID_VIDCAP_VIDEOPROCAMP](/windows-hardware/drivers/stream/propsetid-vidcap-videoprocamp) and [PROPSETID_VIDCAP_CAMERACONTROL](/windows-hardware/drivers/stream/propsetid-vidcap-cameracontrol) control sets provide an allowed range and step value of with which a control can be configured, as well as a default value. For other controls, the caller is responsible for knowing whether the underlying control supports the basic range information.  

Retrieve the range information for a control by calling [IMFCameraControlDefaults::GetRangeInfo](ns-mfidl-mf_camera_control_range_info.md).


## -see-also

[IMFCameraControlDefaults::GetRangeInfo](ns-mfidl-mf_camera_control_range_info.md)