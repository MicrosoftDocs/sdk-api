---
UID: NF:icm.CMCheckColors
title: CMCheckColors
description: Determines whether given colors lie within the output [gamut](/windows/win32/wcs/g) of a specified transform.
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
 - icm.h
api_name:
 - CMCheckColors
f1_keywords:
 - CMCheckColors
 - icm/CMCheckColors
dev_langs:
 - c++
---

## -description

Determines whether given colors lie within the output [gamut](/windows/win32/wcs/g) of a specified transform.

## -parameters

### -param hcmTransform

Handle to the color transform to use.

### -param lpaInputColors

Pointer to an array of [**COLOR**](/windows/win32/api/icm/ns-icm-color) structures to check against the output gamut.

### -param nColors

Specifies the number of elements in the array.

### -param ctInput

Specifies the input color type.

### -param lpaResult

Pointer to a buffer in which to place an array of bytes containing the test results. Each byte in the buffer corresponds to a **COLOR** structure, and on exit has been set to an unsigned value between 0 and 255. The value 0 denotes that the color is in gamut, while a nonzero value indicates that it is out of gamut. For any integer *n* such that 0 \< *n* \< 255, a result value of *n* + 1 indicates that the corresponding color is at least as far out of gamut as would be indicated by a result value of *n*. These values are usually generated from the *gamutTag* in the ICC profile.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. If the function is not successful, the CMM should call [SetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setlasterror) to set the last error to a valid error value defined in Winerror.h.

## -remarks

Every CMM is required to export this function.

If the input color type is not compatible with the color transform **CMCheckColors** fails.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
