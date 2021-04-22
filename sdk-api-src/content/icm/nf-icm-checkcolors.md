---
UID: NF:icm.CheckColors
title: CheckColors
description: Determines whether the colors in an array lie within the output [gamut](/windows/win32/wcs/g) of a specified transform.
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
req.target-min-winverclnt: Windows 2000 Professional \[desktop apps only\]
req.target-min-winversvr: Windows 2000 Server \[desktop apps only\]
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
 - CheckColors
f1_keywords:
 - CheckColors
 - icm/CheckColors
dev_langs:
 - c++
---

## -description

Determines whether the colors in an array lie within the output [gamut](/windows/win32/wcs/g) of a specified transform.

## -parameters

### -param hColorTransform

Handle to the color transform to use.

### -param paInputColors

Pointer to an array of *nColors* [**COLOR**](/windows/win32/api/icm/ns-icm-color) structures to translate.

### -param nColors

Contains the number of elements in the arrays pointed to by *paInputColors* and *paResult*.

### -param ctInput

Specifies the input color type.

### -param paResult

Pointer to an array of *nColors* bytes that receives the results of the test.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

If the input color type is not compatible with the color transform, **CheckColors** fails.

The function places results of the tests in the array pointed to by *paResult*. Each byte in the array corresponds to a **COLOR** element in the array pointed to by *paInputColors* and has an unsigned value between 0 and 255. The value 0 denotes that the color is in gamut, while a nonzero value denotes that it is out of gamut. For any integer *n* such that 0 &lt; *n* &lt; 255, a result value of *n* +1 indicates that the corresponding color is at least as far out of gamut as would be indicated by a result value of *n*.

The out-of-gamut information in the gamut tags created in WCS use the perceptual color distance in CIECAM02, which is the mean square root in CIECAM02 Jab space. The distance in the legacy ICC profile gamut tags is the mean square root in CIELAB space. We recommend that you use the CIECAM02 space when it is available because it provides more perceptually accurate distance metrics.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [COLOR structure](/windows/win32/api/icm/ns-icm-color)
