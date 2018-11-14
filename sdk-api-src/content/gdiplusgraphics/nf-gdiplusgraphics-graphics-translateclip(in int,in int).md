---
UID: NF:gdiplusgraphics.Graphics.TranslateClip(IN INT,IN INT)
title: Graphics::TranslateClip(IN INT,IN INT)
author: windows-sdk-content
description: The Graphics::TranslateClip method translates the clipping region of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_TranslateClip_INT_dx_INT_dy_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicstranslateclipmethods\translateclip.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Graphics class [GDI+],TranslateClip method, Graphics.TranslateClip, Graphics.TranslateClip(IN INT,IN INT), Graphics.TranslateClip(INT,INT), Graphics::TranslateClip, Graphics::TranslateClip(IN INT,IN INT), TranslateClip, TranslateClip method [GDI+], TranslateClip method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_TranslateClip_INT_dx_INT_dy_, gdiplus._gdiplus_CLASS_Graphics_TranslateClip_INT_dx_INT_dy_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusgraphics.h
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
 - Graphics.TranslateClip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gdiplusgraphics.h
: 
- Graphics.TranslateClip
: 
req.product: GDI+ 1.0
---

# Graphics::TranslateClip(IN INT,IN INT)


## -description


The <b>Graphics::TranslateClip</b> method translates the clipping region of this <a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a> object.


## -parameters




### -param dx [in]

Type: <b>INT</b>

Integer that specifies the horizontal component of the translation. 


### -param dy [in]

Type: <b>INT</b>

Integer that specifies the vertical component of the translation. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/58cc052d-31af-4410-81b9-defbad08a1dc">Clipping</a>



<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/5a1f3e79-34c6-4974-a877-3cea75ecb9cc">Graphics::GetClip</a>



<a href="https://msdn.microsoft.com/1a0503da-1d93-4eef-9c0f-dbd257dc8a5d">Graphics::IsClipEmpty</a>



<a href="https://msdn.microsoft.com/52c0b29a-73a8-4bf5-9e8d-950d72d8a9bf">IntersectClip Methods</a>



<a href="https://msdn.microsoft.com/e8348373-da79-4d33-8bea-d594985493d4">SetClip Methods</a>
 

 

