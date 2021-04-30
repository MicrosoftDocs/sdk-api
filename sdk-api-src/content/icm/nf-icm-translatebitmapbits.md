---
UID: NF:icm.TranslateBitmapBits
title: TranslateBitmapBits
description: Translates the colors of a bitmap having a defined format so as to produce another bitmap in a requested format.
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
 - Mscms.dll
api_name:
 - TranslateBitmapBits
f1_keywords:
 - TranslateBitmapBits
 - icm/TranslateBitmapBits
dev_langs:
 - c++
---

## -description

Translates the colors of a bitmap having a defined format so as to produce another bitmap in a requested format.

## -parameters

### -param hColorTransform

Identifies the color transform to use.

### -param pSrcBits

Pointer to the bitmap to translate.

### -param bmInput

Specifies the format of the input bitmap. Must be set to one of the values of the [**BMFORMAT**](/windows/win32/api/icm/ne-icm-bmformat) enumerated type.

> [!Note]  
> This function doesn't support [**BM\_XYZTRIPLETS**](/windows/win32/api/icm/ne-icm-bmformat) or **BM\_YxyTRIPLETS** as inputs.

### -param dwWidth

Specifies the number of pixels per scan line in the input bitmap.

### -param dwHeight

Specifies the number of scan lines in the input bitmap.

### -param dwInputStride

Specifies the number of bytes from the beginning of one scan line to the beginning of the next in the input bitmap; if set to zero, the function assumes that scan lines are padded so as to be **DWORD**-aligned.

### -param pDestBits

Pointer to the buffer in which to place the translated bitmap.

### -param bmOutput

Specifies the format of the output bitmap. Must be set to one of the values of the [**BMFORMAT**](/windows/win32/api/icm/ne-icm-bmformat) enumerated type.

### -param dwOutputStride

Specifies the number of bytes from the beginning of one scan line to the beginning of the next in the output bitmap; if set to zero, the function assumes that scan lines should be padded to be **DWORD**-aligned.

### -param pfnCallBack

Pointer to a callback function called periodically by **TranslateBitmapBits** to report progress and allow the calling process to cancel the translation. (See [**ICMProgressProcCallback**](/windows/win32/wcs/icmprogressproccallback) )

### -param ulCallbackData

Data passed back to the callback function, for example, to identify the translation that is reporting progress.

## -returns

If this function succeeds, the return value is **TRUE**.

If this function fails, the return value is **FALSE**. For extended error information, call **GetLastError**.

## -remarks

If the input and output formats are not compatible with the color transform, this function fails.

When either of the floating point BMFORMATs, BM\_32b\_scARGB or BM\_32b\_scRGB are used, the color data being translated should not contain NaN or infinity. NaN and infinity are not considered to represent legitimate color component values, and the result of translating pixels containing NaN or infinity is meaningless in color terms. NaN or infinity values in the color data being processed will be handled silently, and an error will not be returned.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [ICMProgressProcCallback](/windows/win32/wcs/icmprogressproccallback)
* [Windows bitmap header structures](/windows/win32/wcs/using-structures-in-wcs-1-0)
* [BMFORMAT](/windows/win32/api/icm/ne-icm-bmformat)
