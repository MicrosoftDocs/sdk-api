---
UID: NF:icm.CMTranslateRGBsExt
title: CMTranslateRGBsExt
description: Translates a bitmap from one defined format into a different defined format and calls a callback function periodically, if one is specified, to report progress and permit the calling application to terminate the translation.
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
 - CMTranslateRGBsExt
f1_keywords:
 - CMTranslateRGBsExt
 - icm/CMTranslateRGBsExt
dev_langs:
 - c++
---

## -description

Translates a bitmap from one defined format into a different defined format and calls a callback function periodically, if one is specified, to report progress and permit the calling application to terminate the translation.

## -parameters

### -param hcmTransform

Specifies the color transform to use.

### -param lpSrcBits

Pointer to the bitmap to translate.

### -param bmInput

Specifies the input bitmap format.

### -param dwWidth

Specifies the number of pixels per scan line in the input bitmap.

### -param dwHeight

Specifies the number of scan lines in the input bitmap.

### -param dwInputStride

Specifies the number of bytes from the beginning of one scan line to the beginning of the next in the input bitmap. If *dwInputStride* is set to zero, the CMM should assume that scan lines are padded so as to be **DWORD**-aligned.

### -param lpDestBits

Points to a destination buffer in which to place the translated bitmap.

### -param bmOutput

Specifies the output bitmap format.

### -param dwOutputStride

Specifies the number of bytes from the beginning of one scan line to the beginning of the next in the input bitmap. If *dwOutputStride* is set to zero, the CMM should pad scan lines so that they are **DWORD**-aligned.

### -param lpfnCallback

Pointer to an application-supplied callback function called periodically by **CMTranslateRGBsExt** to report progress and allow the calling process to cancel the translation. (See [**ICMProgressProcCallback**](/windows/win32/wcs/icmprogressproccallback).)

### -param ulCallbackData

Data passed back to the callback function, for example to identify the translation that is reporting progress.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE** and the CMM should call **SetLastError** to set the last error to a valid error value defined in Winerror.h.

## -remarks

Every CMM is required to export this function.

When writing into the destination buffer, the CMM should make sure that scan lines are padded to be **DWORD**-aligned.

If the input and output formats are not compatible with the color transform, this function fails.

If both input and output bitmap formats are 3 channel, 4 bytes per pixel as in the case of BM\_xRGBQUADS, the fourth bytes should be preserved and copied to the output buffer.

If the callback function returns zero, processing should be cancelled and **CMTranslateRGBsExt** should return zero to indicate failure; the output buffer may be partially filled.

Note that this function must support in-place translation. That is, whenever the memory footprint of the output is less than or equal to the memory footprint of the input, this function must be able to translate the bitmap colors even if the source and destination buffers are the same.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts))
* [Functions](/windows/win32/wcs/functions)
