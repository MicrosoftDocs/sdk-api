---
UID: NF:icm.TranslateBitmapBits
title: TranslateBitmapBits function
author: windows-sdk-content
description: The TranslateBitmapBits function translates the colors of a bitmap having a defined format so as to produce another bitmap in a requested format.
old-location: wcs\translatebitmapbits.htm
tech.root: WCS
ms.assetid: c37f821c-fb03-4b98-9ee0-c0ad7fff4685
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: TranslateBitmapBits, TranslateBitmapBits function [Windows Color System], _color_TranslateBitmapBits, icm/TranslateBitmapBits, wcs.translatebitmapbits
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mscms.lib
req.dll: Mscms.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mscms.dll
api_name:
 - TranslateBitmapBits
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TranslateBitmapBits function


## -description


The <b>TranslateBitmapBits</b> function translates the colors of a bitmap having a defined format so as to produce another bitmap in a requested format.


## -parameters




### -param hColorTransform

Identifies the color transform to use.


### -param pSrcBits

Pointer to the bitmap to translate.


### -param bmInput

Specifies the format of the input bitmap. Must be set to one of the values of the <a href="https://msdn.microsoft.com/2388f1b7-af70-4058-a145-abb13159766c">BMFORMAT</a> enumerated type.

<div class="alert"><b>Note</b>  This function does not support <a href="https://msdn.microsoft.com/2388f1b7-af70-4058-a145-abb13159766c">BM_XYZTRIPLETS </a> or <b>BM_YxyTRIPLETS</b> as inputs.</div>
<div> </div>

### -param dwWidth

Specifies the number of pixels per scan line in the input bitmap.


### -param dwHeight

Specifies the number of scan lines in the input bitmap.


### -param dwInputStride

Specifies the number of bytes from the beginning of one scan line to the beginning of the next in the input bitmap; if set to zero, the function assumes that scan lines are padded so as to be <b>DWORD</b>-aligned.


### -param pDestBits

Pointer to the buffer in which to place the translated bitmap.


### -param bmOutput

Specifies the format of the output bitmap. Must be set to one of the values of the <a href="https://msdn.microsoft.com/2388f1b7-af70-4058-a145-abb13159766c">BMFORMAT</a> enumerated type.


### -param dwOutputStride

Specifies the number of bytes from the beginning of one scan line to the beginning of the next in the output bitmap; if set to zero, the function assumes that scan lines should be padded to be <b>DWORD</b>-aligned.


### -param pfnCallBack

TBD


### -param ulCallbackData

Data passed back to the callback function, for example, to identify the translation that is reporting progress.


#### - pfnCallback

Pointer to a callback function called periodically by <b>TranslateBitmapBits</b> to report progress and allow the calling process to cancel the translation. (See <a href="https://msdn.microsoft.com/4e0bfa4c-f0eb-4776-98d6-90d9adf71bee">ICMProgressProcCallback</a> )


## -returns



If this function succeeds, the return value is <b>TRUE</b>.

If this function fails, the return value is <b>FALSE</b>. For extended error information, call <b>GetLastError</b>.




## -remarks



If the input and output formats are not compatible with the color transform, this function fails.

When either of the floating point BMFORMATs, BM_32b_scARGB or BM_32b_scRGB are used, the color data being translated should not contain NaN or infinity. NaN and infinity are not considered to represent legitimate color component values, and the result of translating pixels containing NaN or infinity is meaningless in color terms. NaN or infinity values in the color data being processed will be handled silently, and an error will not be returned.




## -see-also




<a href="https://msdn.microsoft.com/2388f1b7-af70-4058-a145-abb13159766c">BMFORMAT</a>



<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/4e0bfa4c-f0eb-4776-98d6-90d9adf71bee">ICMProgressProcCallback</a>



<a href="using_structures_in_wcs_1_0.htm">Windows Bitmap Header Structures</a>
 

 

