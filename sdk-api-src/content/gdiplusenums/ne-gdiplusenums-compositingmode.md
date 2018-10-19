---
UID: NE:gdiplusenums.CompositingMode
title: CompositingMode
author: windows-sdk-content
description: The CompositingMode enumeration specifies how rendered colors are combined with background colors. This enumeration is used by the Graphics::GetCompositingMode and Graphics::SetCompositingMode methods of the Graphics class.
old-location: gdiplus\_gdiplus_ENUM_CompositingMode.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\compositingmode.htm
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: CompositingMode, CompositingMode enumeration [GDI+], CompositingModeSourceCopy, CompositingModeSourceOver, _gdiplus_ENUM_CompositingMode, gdiplus._gdiplus_ENUM_CompositingMode, gdiplusenums/CompositingMode, gdiplusenums/CompositingModeSourceCopy, gdiplusenums/CompositingModeSourceOver
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: gdiplusenums.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - CompositingMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# CompositingMode enumeration


## -description


The <b>CompositingMode</b> enumeration specifies how rendered colors are combined with background colors. This enumeration is used by the <a href="https://msdn.microsoft.com/en-us/library/ms535700(v=VS.85).aspx">Graphics::GetCompositingMode</a> and <a href="https://msdn.microsoft.com/en-us/library/ms535808(v=VS.85).aspx">Graphics::SetCompositingMode</a> methods of the 
			<b>Graphics</b> class.


## -enum-fields




### -field CompositingModeSourceOver

Specifies that when a color is rendered, it is blended with the background color. The blend is determined by the alpha component of the color being rendered. 


### -field CompositingModeSourceCopy

Specifies that when a color is rendered, it overwrites the background color. This mode cannot be used along with TextRenderingHintClearTypeGridFit. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms535700(v=VS.85).aspx">Graphics::GetCompositingMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535808(v=VS.85).aspx">Graphics::SetCompositingMode</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534404(v=VS.85).aspx">TextRenderingHint</a>
 

 

