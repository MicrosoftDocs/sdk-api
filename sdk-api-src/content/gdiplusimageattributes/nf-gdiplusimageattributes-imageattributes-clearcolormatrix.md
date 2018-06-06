---
UID: NF:gdiplusimageattributes.ImageAttributes.ClearColorMatrix
title: ImageAttributes::ClearColorMatrix
author: windows-sdk-content
description: The ImageAttributes::ClearColorMatrix method clears the color-adjustment matrix for a specified category.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_ClearColorMatrix_type_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\clearcolormatrix.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ClearColorMatrix, ClearColorMatrix method [GDI+], ClearColorMatrix method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],ClearColorMatrix method, ImageAttributes.ClearColorMatrix, ImageAttributes::ClearColorMatrix, _gdiplus_CLASS_ImageAttributes_ClearColorMatrix_type_, gdiplus._gdiplus_CLASS_ImageAttributes_ClearColorMatrix_type_
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - ImageAttributes.ClearColorMatrix
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# ImageAttributes::ClearColorMatrix


## -description


The <b>ImageAttributes::ClearColorMatrix</b> method clears the color-adjustment matrix for a specified category.


## -parameters




### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a> enumeration that specifies the category for which the color-adjustment matrix is cleared. The default value is <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the 	<b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -remarks



An <a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a> object maintains color and grayscale settings for five adjustment categories: default, bitmap, brush, pen, and text. For example, you can specify a color-adjustment matrix for the default category, a different color-adjustment matrix for the bitmap category, and still a different color-adjustment matrix for the pen category.

The default color- and grayscale-adjustment settings apply to all categories that don't have adjustment settings of their own. For example, if you never specify any adjustment settings for the pen category, then the default settings apply to the pen category.

As soon as you specify a color- or grayscale-adjustment setting for a certain category, the default adjustment settings no longer apply to that category. For example, suppose you specify a color-adjustment matrix and a gamma value for the default category. If you set a color-adjustment matrix for the pen category by calling <a href="https://msdn.microsoft.com/6fe73738-41f6-4ff3-bcd5-a885040bf48b">ImageAttributes::SetColorMatrix</a>, then the default color-adjustment matrix will not apply to pens. If you later clear the pen color-adjustment matrix by calling <b>ImageAttributes::ClearColorMatrix</b>, the pen category will not revert to the default adjustment matrix; rather, the pen category will have no adjustment matrix. Similarly, the pen category will not revert to the default gamma value; rather, the pen category will have no gamma value.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/2b37702b-c87f-4f41-8240-a23393019ea3">ColorMatrix</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>



<a href="https://msdn.microsoft.com/4f98fe5b-a1fc-417c-ba08-ddcf0648de21">ImageAttributes::ClearColorMatrices</a>



<a href="https://msdn.microsoft.com/e0e00985-e422-4775-8ee2-a17d97214a25">ImageAttributes::SetColorMatrices</a>



<a href="https://msdn.microsoft.com/6fe73738-41f6-4ff3-bcd5-a885040bf48b">ImageAttributes::SetColorMatrix</a>



<a href="https://msdn.microsoft.com/5b5f673b-f1f4-492e-b012-0c3b27abeeeb">ImageAttributes::SetToIdentity</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/7e018c5a-7933-43b6-b7b3-ee9daea16eb9">Recoloring</a>
 

 

