---
UID: NF:gdiplusimageattributes.ImageAttributes.SetToIdentity
title: ImageAttributes::SetToIdentity
author: windows-sdk-content
description: The ImageAttributes::SetToIdentity method sets the color-adjustment matrix of a specified category to identity matrix.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_SetToIdentity_type_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\settoidentity.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ImageAttributes class [GDI+],SetToIdentity method, ImageAttributes.SetToIdentity, ImageAttributes::SetToIdentity, SetToIdentity, SetToIdentity method [GDI+], SetToIdentity method [GDI+],ImageAttributes class, _gdiplus_CLASS_ImageAttributes_SetToIdentity_type_, gdiplus._gdiplus_CLASS_ImageAttributes_SetToIdentity_type_
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
 - ImageAttributes.SetToIdentity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# ImageAttributes::SetToIdentity


## -description


The <b>ImageAttributes::SetToIdentity</b> method sets the color-adjustment matrix of a specified category to identity matrix.


## -parameters




### -param type [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a> enumeration that specifies the category for which the color-adjustment matrix is set to identity. The default value is <a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustTypeDefault</a>. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534089(v=VS.85).aspx">ColorAdjustType</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534063(v=VS.85).aspx">ColorMatrix</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534464(v=VS.85).aspx">ImageAttributes</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534477(v=VS.85).aspx">Metafile</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533809(v=VS.85).aspx">Recoloring</a>
 

 

