---
UID: NF:gdiplusheaders.Bitmap.ApplyEffect(Bitmap,INT,Effect,RECT,RECT,Bitmap)
title: Bitmap::ApplyEffect(IN Bitmap,IN INT,IN Effect,IN RECT,OUT RECT,OUT Bitmap) (gdiplusheaders.h)
description: The Bitmap::ApplyEffect method creates a new Bitmap object by applying a specified effect to an existing Bitmap object.
helpviewer_keywords: ["ApplyEffect","ApplyEffect method [GDI+]","ApplyEffect method [GDI+]","Bitmap class","Bitmap class [GDI+]","ApplyEffect method","Bitmap.ApplyEffect","Bitmap.ApplyEffect(Bitmap**","INT","Effect*","RECT*","RECT*","Bitmap**)","Bitmap.ApplyEffect(IN Bitmap","IN INT","IN Effect","IN RECT","OUT RECT","OUT Bitmap)","Bitmap::ApplyEffect","Bitmap::ApplyEffect(IN Bitmap","IN INT","IN Effect","IN RECT","OUT RECT","OUT Bitmap)","_gdiplus_CLASS_Bitmap_ApplyEffect_Bitmap_inputs_","gdiplus._gdiplus_CLASS_Bitmap_ApplyEffect_Bitmap_inputs_"]
old-location: gdiplus\_gdiplus_CLASS_Bitmap_ApplyEffect_Bitmap_inputs_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapapplyeffectmethods\applyeffect_bitmapinputs.htm
ms.date: 12/05/2018
ms.keywords: ApplyEffect, ApplyEffect method [GDI+], ApplyEffect method [GDI+],Bitmap class, Bitmap class [GDI+],ApplyEffect method, Bitmap.ApplyEffect, Bitmap.ApplyEffect(Bitmap**,INT,Effect*,RECT*,RECT*,Bitmap**), Bitmap.ApplyEffect(IN Bitmap,IN INT,IN Effect,IN RECT,OUT RECT,OUT Bitmap), Bitmap::ApplyEffect, Bitmap::ApplyEffect(IN Bitmap,IN INT,IN Effect,IN RECT,OUT RECT,OUT Bitmap), _gdiplus_CLASS_Bitmap_ApplyEffect_Bitmap_inputs_, gdiplus._gdiplus_CLASS_Bitmap_ApplyEffect_Bitmap_inputs_
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
ms.custom: 19H1
f1_keywords:
 - Bitmap::ApplyEffect
 - gdiplusheaders/Bitmap::ApplyEffect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Bitmap.ApplyEffect
---

# Bitmap::ApplyEffect(IN Bitmap,IN INT,IN Effect,IN RECT,OUT RECT,OUT Bitmap)


## -description

The <b>Bitmap::ApplyEffect</b> method  creates a new <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object by applying a specified effect to an existing <b>Bitmap</b> object.

## -parameters

### -param inputs [in]

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>**</b>

Address of a pointer to a <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object to which the effect is applied.

### -param numInputs [in]

Type: <b>INT</b>

Integer that specifies the number of input bitmaps. This parameter must be set to 1.

### -param effect [in]

Type: <b><a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-effect">Effect</a>*</b>

Pointer to an instance of a descendant of the <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-effect">Effect</a> class. The descendant (for example, a <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-blur">Blur</a> object) specifies the effect that is applied.

### -param ROI [in]

Type: <b>RECT*</b>

Pointer to a RECT structure that specifies the portion of the input bitmap that is used.

### -param outputRect [out]

Type: <b>RECT*</b>

Pointer to a RECT structure that receives the portion of the input bitmap that was used. If the rectangle specified by <i>ROI</i> lies entirely within the input bitmap, the rectangle returned in <i>outputRect</i> is the same as <i>ROI</i>. If part of rectangle specified by <i>ROI</i> lies outside the input bitmap, then the rectangle returned in <i>outputRect</i> is the portion of <i>ROI</i> that lies within the input bitmap. Pass <b>NULL</b> if you do not want to receive the output rectangle.

### -param output [out]

Type: <b><a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>**</b>

Address of a variable that receives a pointer to the new <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -remarks

<b>Bitmap::ApplyEffect</b> returns a pointer to a new <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> object. When you have finished using that <b>Bitmap</b> object, call <a href="/windows/desktop/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete">delete</a> to free the memory that it occupies.


#### Examples



The following example creates two <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a> objects: <b>inputBitmap</b> and <b>outputBitmap</b>. First, <b>inputBitmap</b> is constructed from a BMP file. Then <b>outputBitmap</b> is created by passing the address of <b>inputBitmap</b> to the <b>Bitmap::ApplyEffect</b> method. <b>Bitmap::ApplyEffect</b> takes the portion of <b>inputBitmap</b> specified by <b>rectOfInterest</b> and increases the contrast as specified by <b>briCon</b>, a <a href="/windows/desktop/api/gdipluseffects/nl-gdipluseffects-brightnesscontrast">BrightnessContrast</a> object.


```cpp
VOID Example_BrightnessContrastApplyEffect2(HDC hdc)
{
   Graphics graphics(hdc);
   Bitmap* inputBitmap = new Bitmap(L"Picture.bmp");
   Bitmap* outputBitmap = NULL;  
   RECT rectOfInterest = {10, 12, 100, 80};
  
   BrightnessContrastParams briConParams;
   briConParams.brightnessLevel = 0;
   briConParams.contrastLevel = 25;
   BrightnessContrast briCon;
   briCon.SetParameters(&briConParams);

   // Draw the original image.
   graphics.DrawImage(inputBitmap, 20, 20);

   // Apply the change in contrast.
   Bitmap::ApplyEffect(
      &inputBitmap, 1, &briCon, &rectOfInterest, NULL, &outputBitmap);

   // Draw the new image.
   graphics.DrawImage(outputBitmap, 200, 20);

   delete inputBitmap;
   delete outputBitmap;
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect Methods</a>