---
UID: NF:mfidl.IMFCameraControlDefaults.GetType
tech.root: mf
title: IMFCameraControlDefaults::GetType
ms.date: 05/06/2022
targetos: Windows
description: Gets the configuration type of the control, indicating whether the control value must be set  before streaming begins or after streaming has started.
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
 - IMFCameraControlDefaults::GetType
f1_keywords:
 - IMFCameraControlDefaults::GetType
 - mfidl/IMFCameraControlDefaults::GetType
dev_langs:
 - c++
helpviewer_keywords:
 - GetType
---

## -description

Gets the configuration type of the control, indicating whether the control value must be set  before streaming begins or after streaming has started.

## -returns

A member of the [MF_SENSOR_CONTROL_CONFIGURATION_TYPE](ne-mfidl-mf_camera_control_configuration_type.md) enumeration specifying the configuration type of the control.

## -remarks

Some sensor-level controls can only be set after the sensor has started (such as focus/brightness/whitebalance) since the controls require frame data for the parameters to converge. Other types of controls, such as HDR support, can only be configured when the sensor is not in a running state because it requires a re-programming of the sensor mode. Whether a well known control is pre or post start is specified in the DDI specification of the control. If the DDI specification does not explicitly indicate the a control is a pre-start control, the caller should assume the control is post-start.  

## -see-also

