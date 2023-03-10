---
UID: NE:mfidl.__MIDL___MIDL_itf_mfidl_0000_0136_0001
tech.root: mf
title: MF_CAMERA_CONTROL_CONFIGURATION_TYPE
ms.date: 05/05/2022
targetos: Windows
description: Specifies the configuration type of a camera control.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: mfidl.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: Windows 11 Build 22621
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - __MIDL___MIDL_itf_mfidl_0000_0136_0001
 - MF_CAMERA_CONTROL_CONFIGURATION_TYPE
f1_keywords:
 - __MIDL___MIDL_itf_mfidl_0000_0136_0001
 - mfidl/__MIDL___MIDL_itf_mfidl_0000_0136_0001
 - MF_CAMERA_CONTROL_CONFIGURATION_TYPE
 - mfidl/MF_CAMERA_CONTROL_CONFIGURATION_TYPE
dev_langs:
 - c++
helpviewer_keywords:
 - __MIDL___MIDL_itf_mfidl_0000_0136_0001
---

## -description

Specifies the configuration type of a camera control.

## -enum-fields

### -field MF_CAMERA_CONTROL_CONFIGURATION_TYPE_PRESTART

The camera control must be configured before streaming begins.

### -field MF_CAMERA_CONTROL_CONFIGURATION_TYPE_POSTSTART

The camera control must be  configured after streaming has started.

## -remarks

Some sensor-level controls can only be set after the sensor has started (such as focus/brightness/whitebalance) since the controls require frame data for the parameters to converge. Other types of controls, such as HDR support, can only be configured when the sensor is not in a running state because it requires a re-programming of the sensor mode. Whether a well known control is pre or post start is specified in the DDI specification of the control. If the DDI specification does not explicitly indicate the a control is a pre-start control, the caller should assume the control is post-start.  

Retrieve the configuration type of a control by calling [IMFCameraControlDefaults::GetType](ne-mfidl-mf_camera_control_configuration_type.md).


## -see-also

 [IMFCameraControlDefaults::GetType](ne-mfidl-mf_camera_control_configuration_type.md)