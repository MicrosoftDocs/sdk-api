---
UID: NF:gdiplusimageattributes.ImageAttributes.SetNoOp
title: ImageAttributes::SetNoOp (gdiplusimageattributes.h)
author: windows-sdk-content
description: The ImageAttributes::SetNoOp method turns off color adjustment for a specified category. You can call ImageAttributes::ClearNoOp to reinstate the color-adjustment settings that were in place before the call to ImageAttributes::SetNoOp.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetNoOp_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\setnoop.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ImageAttributes class [GDI+],SetNoOp method, ImageAttributes.SetNoOp, ImageAttributes::SetNoOp, SetNoOp, SetNoOp method [GDI+], SetNoOp method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetNoOp_type_, gdiplus._gdiplus_CLASS_ImageAttributes_SetNoOp_type_
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - ImageAttributes.SetNoOp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# ImageAttributes::SetNoOp


## -description


The <b>ImageAttributes::SetNoOp</b> method turns off color adjustment for a specified category. You can call <a href="https://msdn.microsoft.com/en-us/library/ms535419(v=VS.85).aspx">ImageAttributes::ClearNoOp</a> to reinstate the color-adjustment settings that were in place before the call to <b>ImageAttributes::SetNoOp</b>.


## -parameters




### -param type [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a> enumeration that specifies the category for which color correction is turned off. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535419(v=VS.85).aspx">ImageAttributes::ClearNoOp</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535427(v=VS.85).aspx">ImageAttributes::Reset</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535438(v=VS.85).aspx">ImageAttributes::SetToIdentity</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533809(v=VS.85).aspx">Recoloring</a>
 

 

