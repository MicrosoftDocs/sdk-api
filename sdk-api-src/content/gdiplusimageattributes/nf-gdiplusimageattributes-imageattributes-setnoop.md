---
UID: NF:gdiplusimageattributes.ImageAttributes.SetNoOp
title: ImageAttributes::SetNoOp
author: windows-driver-content
description: The ImageAttributes::SetNoOp method turns off color adjustment for a specified category. You can call ImageAttributes::ClearNoOp to reinstate the color-adjustment settings that were in place before the call to ImageAttributes::SetNoOp.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetNoOp_type_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setnoop.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ImageAttributes class [GDI+],SetNoOp method, ImageAttributes.SetNoOp, ImageAttributes::SetNoOp, SetNoOp, SetNoOp method [GDI+], SetNoOp method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetNoOp_type_, gdiplus._gdiplus_CLASS_ImageAttributes_SetNoOp_type_
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
-	ImageAttributes.SetNoOp
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# ImageAttributes::SetNoOp


## -description


The <b>ImageAttributes::SetNoOp</b> method turns off color adjustment for a specified category. You can call <a href="https://msdn.microsoft.com/ffb07a2d-2b85-4dd2-8885-a30cea749b01">ImageAttributes::ClearNoOp</a> to reinstate the color-adjustment settings that were in place before the call to <b>ImageAttributes::SetNoOp</b>.


## -parameters




### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a> enumeration that specifies the category for which color correction is turned off. The default value is <a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545216">Bitmap</a>



<a href="https://msdn.microsoft.com/1bae1b30-2268-46e2-9cfa-2ee606180af6">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/fbb107d2-b079-4916-89bb-d61fcd860894">ImageAttributes</a>



<a href="https://msdn.microsoft.com/ffb07a2d-2b85-4dd2-8885-a30cea749b01">ImageAttributes::ClearNoOp</a>



<a href="https://msdn.microsoft.com/27292b56-4bca-41bd-8923-b1d0e1a97c5e">ImageAttributes::Reset</a>



<a href="https://msdn.microsoft.com/5b5f673b-f1f4-492e-b012-0c3b27abeeeb">ImageAttributes::SetToIdentity</a>



<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a>



<a href="https://msdn.microsoft.com/7e018c5a-7933-43b6-b7b3-ee9daea16eb9">Recoloring</a>
 

 

