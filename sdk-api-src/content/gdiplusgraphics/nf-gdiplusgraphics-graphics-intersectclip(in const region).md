---
UID: NF:gdiplusgraphics.Graphics.IntersectClip(IN const Region)
title: Graphics::IntersectClip(IN const Region)
author: windows-sdk-content
description: The Graphics::IntersectClip method updates the clipping region of this Graphics object to the portion of the specified region that intersects with the current clipping region of this Graphics object.
old-location: gdiplus\_gdiplus_CLASS_Graphics_IntersectClip_region_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\graphicsintersectclipmethods\intersectclip_28region.htm
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Graphics class [GDI+],IntersectClip method, Graphics.IntersectClip, Graphics.IntersectClip(IN const Region), Graphics.IntersectClip(const Region*), Graphics::IntersectClip, Graphics::IntersectClip(IN const Region), IntersectClip, IntersectClip method [GDI+], IntersectClip method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_IntersectClip_region_, gdiplus._gdiplus_CLASS_Graphics_IntersectClip_region_
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
 - Graphics.IntersectClip
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
- Graphics.IntersectClip
: 
req.product: GDI+ 1.0
---

# Graphics::IntersectClip(IN const Region)


## -description


The <b>Graphics::IntersectClip</b> method updates the clipping region of this 
			<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object to the portion of the specified region that intersects with the current clipping region of this 
			<b>Graphics</b> object.


## -parameters




### -param region [in]

Type: <b>const Region*</b>

Pointer to a region that is used to update the clipping region of this 
					<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/58cc052d-31af-4410-81b9-defbad08a1dc">Clipping</a>



<a href="https://msdn.microsoft.com/816a5845-ca03-46c6-bdda-e6a7d02ff614">Clipping with a Region</a>



<a href="https://msdn.microsoft.com/b46ce1d3-c2b5-4dbf-86b7-2e6f52ab2787">GetClipBounds Methods</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/5a1f3e79-34c6-4974-a877-3cea75ecb9cc">Graphics::GetClip</a>



<a href="https://msdn.microsoft.com/2972b879-7d2f-4cad-b17d-670125f43691">Region</a>



<a href="https://msdn.microsoft.com/e8348373-da79-4d33-8bea-d594985493d4">SetClip Methods</a>
 

 

