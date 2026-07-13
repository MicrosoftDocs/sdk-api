---
UID: NF:icm.CMDeleteTransform
title: CMDeleteTransform
description: Deletes a specified color transform, and frees any memory associated with it.
tech.root: wcs
ms.date: 02/01/2021
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: icm.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Icm32.Lib
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
 - icm32.dll
api_name:
 - CMDeleteTransform
f1_keywords:
 - CMDeleteTransform
 - icm/CMDeleteTransform
dev_langs:
 - c++
---

## -description

Deletes a specified color transform, and frees any memory associated with it.

## -parameters

### -param hcmTransform

Identifies the color transform to be deleted.

## -returns

If this function succeeds, the return value is **TRUE**.

If the function fails, the return value is **FALSE**. If the **CMDeleteTransform** function is not successful, the CMM should call **SetLastError** to set the last error to a valid error value defined in Winerror.h.

## -remarks

Every CMM is required to export this function.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
