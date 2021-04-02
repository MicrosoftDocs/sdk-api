---
UID: NF:icm.CheckBitmapBits
title: CheckBitmapBits
description: Checks whether the pixels in a specified bitmap lie within the output [gamut](/windows/win32/wcs/g) of a specified transform.
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
 - CheckBitmapBits
f1_keywords:
 - CheckBitmapBits
 - icm/CheckBitmapBits
dev_langs:
 - c++
---

## -description

Checks whether the pixels in a specified bitmap lie within the output [gamut](/windows/win32/wcs/g) of a specified transform.

## -parameters

### -param hColorTransform

Handle to the color transform to use.

### -param pSrcBits

Pointer to the bitmap to check against the output gamut.

### -param bmInput

Specifies the format of the bitmap. Must be set to one of the values of the [**BMFORMAT**](/windows/win32/api/icm/ne-icm-bmformat) enumerated type.

### -param dwWidth

Specifies the number of pixels per scan line of the bitmap.

### -param dwHeight

Specifies the number of scan lines of the bitmap.

### -param dwStride

Specifies the number of bytes from the beginning one scan line to the beginning of the next one. If set to zero, the bitmap scan lines are assumed to be padded so as to be **DWORD**-aligned.

### -param paResult

Pointer to an array of bytes where the test results are to be placed. This results buffer must contain at least as many bytes as there are pixels in the bitmap.

### -param pfnCallback

Pointer to a callback function called periodically by **CheckBitmapBits** to report progress and allow the calling process to cancel the bitmap test. (See [**ICMProgressProcCallback**](/windows/win32/wcs/icmprogressproccallback)).  

### -param lpCallbackData

Data passed back to the callback function, for example, to identify the bitmap test about which progress is being reported.

## -returns

If this function succeeds, the return value is a nonzero value.

If this function fails, the return value is zero. For extended error information, call **GetLastError**.

## -remarks

If the input format is not compatible with the color transform, the **CheckBitmapBits** function fails.

This function places results of the tests in the buffer pointed to by *paResult*. Each byte in the buffer corresponds to a pixel in the bitmap, and has an unsigned value between 0 and 255. The value 0 denotes that the color is in gamut, while a nonzero value denotes that it is out of gamut. For any integer *n* such that 0 &lt;*n* &lt; 255, a result value of *n* + 1 indicates that the corresponding color is at least as far out of gamut as would be indicated by a result value of *n*.

When either of the floating point BMFORMATs, BM\_32b\_scARGB or BM\_32b\_scRGB is used, the color data being checked should not contain NaN or infinity. NaN and infinity are not considered to represent legitimate color component values, and the result of checking pixels containing NaN or infinity is meaningless in color terms. NaN or infinity values in the color data being processed will be handled silently, and an error will not be returned.

The out-of-gamut information in the gamut tags created in WCS use the perceptual color distance in CIECAM02, which is the mean square root in CIECAM02 Jab space. The distance in the legacy ICC profile gamut tags is the mean square root in CIELAB space. We recommend that you use the CIECAM02 space when it is available because it provides more perceptually accurate distance metrics.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [ICMProgressProcCallback](/windows/win32/wcs/icmprogressproccallback)
* [BMFORMAT](/windows/win32/api/icm/ne-icm-bmformat)
