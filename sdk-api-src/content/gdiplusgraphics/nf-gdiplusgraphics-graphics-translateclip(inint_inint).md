---
UID: NF:gdiplusgraphics.Graphics.TranslateClip(IN INT,IN INT)
title: Graphics::TranslateClip(IN INT,IN INT) (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::TranslateClip method translates the clipping region of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_TranslateClip_INT_dx_INT_dy_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicstranslateclipmethods\translateclip.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],TranslateClip method, Graphics.TranslateClip, Graphics.TranslateClip(IN INT,IN INT), Graphics.TranslateClip(INT,INT), Graphics::TranslateClip, Graphics::TranslateClip(IN INT,IN INT), TranslateClip, TranslateClip method [GDI+], TranslateClip method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_TranslateClip_INT_dx_INT_dy_, gdiplus._gdiplus_CLASS_Graphics_TranslateClip_INT_dx_INT_dy_
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
req.product: GDI+ 1.0
ms.custom: 19H1
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



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms536360(v=VS.85).aspx">Clipping</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533825(v=VS.85).aspx">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534453(v=VS.85).aspx">Graphics</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535698(v=VS.85).aspx">Graphics::GetClip</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535792(v=VS.85).aspx">Graphics::IsClipEmpty</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535783(v=VS.85).aspx">IntersectClip Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535789(v=VS.85).aspx">SetClip Methods</a>
 

 

