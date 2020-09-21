---
UID: NF:gdiplusheaders.Bitmap.ApplyEffect(Effect,RECT)
title: Bitmap::ApplyEffect
description: The Bitmap::ApplyEffect method alters this Bitmap object by applying a specified effect.
tech.root: gdiplus
helpviewer_keywords: ["Bitmap::ApplyEffect"]
ms.assetid: fff2c151-92df-477e-aafd-6aaca27df414
ms.date: 05/20/2019
ms.keywords: Bitmap::ApplyEffect
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: gdiplusheaders.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - Bitmap::ApplyEffect
 - gdiplusheaders/Bitmap::ApplyEffect
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - Bitmap::ApplyEffect
---

# ApplyEffect(Effect*,RECT*)


## -description

The **Bitmap::ApplyEffect** method alters this <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object by applying a specified effect.

## -parameters

### -param effect

Pointer to an instance of a descendant of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-effect">Effect</a> class.
The descendant (for example, a <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-blur">Blur</a> object) specifies the effect that is applied.

### -param ROI

Pointer to a **RECT** structure that specifies the portion of the input bitmap to which the effect is applied.
Pass **NULL** to specify that the effect applies to the entire input bitmap.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

#### Examples

The following example draws an image twice: once with no change, and once after the brightness has been increased for part of the image.

```cpp
VOID Example_BrightnessContrastApplyEffect1(HDC hdc)
{
   Graphics graphics(hdc);
   Bitmap myBitmap(L"Picture.bmp");
   UINT srcWidth = myBitmap.GetWidth();
   UINT srcHeight = myBitmap.GetHeight();

   BrightnessContrastParams briConParams;
   briConParams.brightnessLevel = 50;
   briConParams.contrastLevel = 0;
   BrightnessContrast briCon;
   briCon.SetParameters(&briConParams);
   RECT rectOfInterest = {20, 15, 80, 50};

   // Draw the original image.
   graphics.DrawImage(&myBitmap, 20, 20, srcWidth, srcHeight);

   // Increase the brightness in a portion of the image.
   myBitmap.ApplyEffect(&briCon, &rectOfInterest);

   // Draw the image again.
   graphics.DrawImage(&myBitmap, 200, 20, srcWidth, srcHeight);
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>