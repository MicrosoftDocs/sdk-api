---
UID: NL:gdiplusimageattributes.ImageAttributes
title: ImageAttributes (gdiplusimageattributes.h)
author: windows-sdk-content
description: An ImageAttributes object contains information about how bitmap and metafile colors are manipulated during rendering.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributes.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ImageAttributes, ImageAttributes class [GDI+], ImageAttributes class [GDI+],described, _gdiplus_CLASS_ImageAttributes_Class, gdiplus._gdiplus_CLASS_ImageAttributes_Class, gdiplusimageattributes/ImageAttributes
ms.topic: class
req.header: gdiplusimageattributes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdiplusimageattributes.h
api_name:
 - ImageAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImageAttributes class


## -description


An <a href="https://msdn.microsoft.com/en-us/library/ms535413(v=VS.85).aspx">ImageAttributes</a> object contains information about how bitmap and metafile colors are manipulated during rendering. An <b>ImageAttributes</b> object maintains several color-adjustment settings, including color-adjustment matrices, grayscale-adjustment matrices, gamma-correction values, color-map tables, and color-threshold values.


## -remarks



The colors in an image can be manipulated during rendering. They can be corrected, darkened, lightened, removed, and so on. To apply such manipulations, initialize an <a href="https://msdn.microsoft.com/en-us/library/ms535413(v=VS.85).aspx">ImageAttributes</a> object and pass the address of that <b>ImageAttributes</b> object (along with the address of an 
				<a href="https://msdn.microsoft.com/en-us/library/ms535365(v=VS.85).aspx">Image</a> object) to the 
				<a href="https://msdn.microsoft.com/en-us/library/ms536028(v=VS.85).aspx">Graphics::DrawImage</a> method. 



