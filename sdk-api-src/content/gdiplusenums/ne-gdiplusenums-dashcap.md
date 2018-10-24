---
UID: NE:gdiplusenums.DashCap
title: DashCap
author: windows-sdk-content
description: The DashCap enumeration specifies the type of graphic shape to use on both ends of each dash in a dashed line.
old-location: gdiplus\_gdiplus_ENUM_DashCap.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\dashcap.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: DashCap, DashCap enumeration [GDI+], DashCapFlat, DashCapRound, DashCapTriangle, _gdiplus_ENUM_DashCap, gdiplus._gdiplus_ENUM_DashCap, gdiplusenums/DashCap, gdiplusenums/DashCapFlat, gdiplusenums/DashCapRound, gdiplusenums/DashCapTriangle
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
 - DashCap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# DashCap enumeration


## -description


The <b>DashCap</b> enumeration specifies the type of graphic shape to use on both ends of each dash in a dashed line.


## -enum-fields




### -field DashCapFlat

Specifies a square cap that squares off both ends of each dash. 


### -field DashCapRound

Specifies a circular cap that rounds off both ends of each dash. 


### -field DashCapTriangle

Specifies a triangular cap that points both ends of each dash. 


## -remarks



If you set the alignment of a 
				<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> object to <b>PenAlignmentInset</b>, you cannot use that pen to draw triangular dash caps.



