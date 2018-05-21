---
UID: NF:gdiplusimageattributes.ImageAttributes.SetColorMatrix
title: ImageAttributes::SetColorMatrix
author: windows-driver-content
description: The ImageAttributes::SetColorMatrix method sets the color-adjustment matrix for a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetColorMatrix_colorMatrix_mode_type_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setcolormatrix.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: ImageAttributes class [GDI+],SetColorMatrix method, ImageAttributes.SetColorMatrix, ImageAttributes::SetColorMatrix, SetColorMatrix, SetColorMatrix method [GDI+], SetColorMatrix method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetColorMatrix_colorMatrix_mode_type_, gdiplus._gdiplus_CLASS_ImageAttributes_SetColorMatrix_colorMatrix_mode_type_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusimageattributes.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	ImageAttributes.SetColorMatrix
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# ImageAttributes::SetColorMatrix


## -description


The <b>ImageAttributes::SetColorMatrix</b> method sets the color-adjustment matrix for a specified category.


## -parameters




### -param colorMatrix [in]

Type: <b>const <a href="https://msdn.microsoft.com/2b37702b-c87f-4f41-8240-a23393019ea3">ColorMatrix</a>*</b>

Pointer to a 5×5 color-adjustment matrix. 


### -param mode [in]

Type: <b><a href="https://msdn.microsoft.com/e5c55c49-2369-4775-8d54-2b1c287675d5">ColorMatrixFlags</a></b>

Element of the <a href="https://msdn.microsoft.com/e5c55c49-2369-4775-8d54-2b1c287675d5">ColorMatrixFlags</a> enumeration that specifies the type of image and color that will be affected by the color-adjustment matrix. 


### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a> enumeration that specifies the category for which the color-adjustment matrix is set. The default value is <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



An <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a color-adjustment matrix for the default category, a different color-adjustment matrix for the bitmap category, and still a different color-adjustment matrix for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a collection of adjustment settings for the default category. If you set the color-adjustment matrix for the pen category by passing <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustTypePen</a> to the <b>ImageAttributes::SetColorMatrix</b> method, then none of the default adjustment settings will apply to pens.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/2b37702b-c87f-4f41-8240-a23393019ea3">ColorMatrix</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>



<a href="https://msdn.microsoft.com/4f98fe5b-a1fc-417c-ba08-ddcf0648de21">ImageAttributes::ClearColorMatrices</a>



<a href="https://msdn.microsoft.com/2043d592-e79a-45ce-8964-25ed245e4373">ImageAttributes::ClearColorMatrix</a>



<a href="https://msdn.microsoft.com/e0e00985-e422-4775-8ee2-a17d97214a25">ImageAttributes::SetColorMatrices</a>



<a href="https://msdn.microsoft.com/5b5f673b-f1f4-492e-b012-0c3b27abeeeb">ImageAttributes::SetToIdentity</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/7e018c5a-7933-43b6-b7b3-ee9daea16eb9">Recoloring</a>
 

 

