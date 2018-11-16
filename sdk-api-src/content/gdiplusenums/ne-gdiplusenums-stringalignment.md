---
UID: NE:gdiplusenums.StringAlignment
title: StringAlignment
author: windows-sdk-content
description: The StringAlignment enumeration specifies how a string is aligned in reference to the bounding rectangle. A bounding rectangle is used to define the area in which the text displays.
old-location: gdiplus\_gdiplus_ENUM_StringAlignment.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\stringalignment.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: StringAlignment, StringAlignment enumeration [GDI+], StringAlignmentCenter, StringAlignmentFar, StringAlignmentNear, _gdiplus_ENUM_StringAlignment, gdiplus._gdiplus_ENUM_StringAlignment, gdiplusenums/StringAlignment, gdiplusenums/StringAlignmentCenter, gdiplusenums/StringAlignmentFar, gdiplusenums/StringAlignmentNear
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
 - StringAlignment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# StringAlignment enumeration


## -description


The <b>StringAlignment</b> enumeration specifies how a string is aligned in reference to the bounding rectangle. A bounding rectangle is used to define the area in which the text displays.


## -enum-fields




### -field StringAlignmentNear

Specifies that alignment is towards the origin of the bounding rectangle. May be used for alignment of characters along the line or for alignment of lines within the rectangle. For a right to left bounding rectangle (<a href="https://msdn.microsoft.com/9bbddab0-46b1-49db-86c1-cf9086692958">StringFormatFlagsDirectionRightToLeft</a>), the origin is at the upper right. 


### -field StringAlignmentCenter

Specifies that alignment is centered between origin and extent (width) of the formatting rectangle. 


### -field StringAlignmentFar

Specifies that alignment is to the far extent (right side) of the formatting rectangle. 

