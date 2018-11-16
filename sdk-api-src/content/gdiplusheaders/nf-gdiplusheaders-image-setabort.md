---
UID: NF:gdiplusheaders.Image.SetAbort
title: Image::SetAbort
author: windows-sdk-content
description: The Image::SetAbort method sets the object whose Abort method is called periodically during time-consuming rendering operation.
old-location: gdiplus\_gdiplus_CLASS_Image_SetAbort_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageclass\imagemethods\setabort.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Image class [GDI+],SetAbort method, Image.SetAbort, Image::SetAbort, SetAbort, SetAbort method [GDI+], SetAbort method [GDI+],Image class, _gdiplus_CLASS_Image_SetAbort_, gdiplus._gdiplus_CLASS_Image_SetAbort_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Image.SetAbort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusheaders.h
: 
- Image.SetAbort
: 
req.product: GDI+ 1.1
---

# Image::SetAbort


## -description


The <b>Image::SetAbort</b> method sets the object whose <b>Abort</b> method is called periodically during time-consuming rendering operation.


## -parameters




### -param pIAbort

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534066(v=VS.85).aspx">GdiplusAbort</a>*</b>

Pointer to an application-defined descendant of the <a href="https://msdn.microsoft.com/en-us/library/ms534066(v=VS.85).aspx">GdiplusAbort</a> structure.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534462(v=VS.85).aspx">Image</a>
 

 

