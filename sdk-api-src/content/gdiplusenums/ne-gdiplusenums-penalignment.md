---
UID: NE:gdiplusenums.PenAlignment
title: PenAlignment
author: windows-sdk-content
description: The PenAlignment enumeration specifies the alignment of a pen relative to the stroke that is being drawn.
old-location: gdiplus\_gdiplus_ENUM_PenAlignment.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\penalignment.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PenAlignment, PenAlignment enumeration [GDI+], PenAlignmentCenter, PenAlignmentInset, _gdiplus_ENUM_PenAlignment, gdiplus._gdiplus_ENUM_PenAlignment, gdiplusenums/PenAlignment, gdiplusenums/PenAlignmentCenter, gdiplusenums/PenAlignmentInset
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - PenAlignment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# PenAlignment enumeration


## -description


The <b>PenAlignment</b> enumeration specifies the alignment of a pen relative to the stroke that is being drawn.


## -enum-fields




### -field PenAlignmentCenter

Specifies that the pen is aligned on the center of the line that is drawn. 


### -field PenAlignmentInset

Specifies, when drawing a polygon, that the pen is aligned on the inside of the edge of the polygon. 


## -remarks



If you set the alignment of a 
				<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object to <b><b>PenAlignmentInset</b></b>, you cannot use that pen to draw compound lines or triangular dash caps.



