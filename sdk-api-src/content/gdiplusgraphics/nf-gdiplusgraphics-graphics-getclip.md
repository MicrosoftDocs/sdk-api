---
UID: NF:gdiplusgraphics.Graphics.GetClip
title: Graphics::GetClip
author: windows-driver-content
description: The Graphics::GetClip method gets the clipping region of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_GetClip_region_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\getclip.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetClip, GetClip method [GDI+], GetClip method [GDI+],Graphics class, Graphics class [GDI+],GetClip method, Graphics.GetClip, Graphics::GetClip, _gdiplus_CLASS_Graphics_GetClip_region_, gdiplus._gdiplus_CLASS_Graphics_GetClip_region_
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gdiplus.dll
api_name:
-	Graphics.GetClip
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::GetClip


## -description


The <b>Graphics::GetClip</b> method gets the clipping region of this 
			<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object.


## -parameters




### -param region [out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn915769">Region</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915769">Region</a> object that receives the clipping region. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method
fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/58cc052d-31af-4410-81b9-defbad08a1dc">Clipping</a>



<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/b46ce1d3-c2b5-4dbf-86b7-2e6f52ab2787">GetClipBounds Methods</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/f3fcb50c-30c3-4a57-ab99-ebe7d05ede8f">Graphics::ResetClip</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn915769">Region</a>



<a href="https://msdn.microsoft.com/e8348373-da79-4d33-8bea-d594985493d4">SetClip Methods</a>
 

 

