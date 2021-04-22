---
UID: NF:icm.WcsSetCalibrationManagementState
title: WcsSetCalibrationManagementState
description: Enables or disables system management of the display calibration state.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Mscms.dll
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Mscms.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
api_location:
 - mscms.dll
api_name:
 - WcsSetCalibrationManagementState
f1_keywords:
 - WcsSetCalibrationManagementState
 - icm/WcsSetCalibrationManagementState
dev_langs:
 - c++
---

## -description

Enables or disables system management of the display calibration state.

## -parameters

### -param bIsEnabled

**TRUE** to enable system management of the display calibration state. **FALSE** to disable system management of the display calibration state.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**.

## -remarks

This function must be called with elevated permissions for it to succeed.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
