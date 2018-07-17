---
UID: NE:gdiplusenums.DashStyle
title: DashStyle
author: windows-sdk-content
description: The DashStyle enumeration specifies the line style of a line drawn with a Windows GDI+ pen. The line can be drawn by using one of several predefined styles or a custom style.
old-location: gdiplus\_gdiplus_ENUM_DashStyle.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\dashstyle.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: DashStyle, DashStyle enumeration [GDI+], DashStyleCustom, DashStyleDash, DashStyleDashDot, DashStyleDashDotDot, DashStyleDot, DashStyleSolid, _gdiplus_ENUM_DashStyle, gdiplus._gdiplus_ENUM_DashStyle, gdiplusenums/DashStyle, gdiplusenums/DashStyleCustom, gdiplusenums/DashStyleDash, gdiplusenums/DashStyleDashDot, gdiplusenums/DashStyleDashDotDot, gdiplusenums/DashStyleDot, gdiplusenums/DashStyleSolid
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - DashStyle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# DashStyle enumeration


## -description


The <b>DashStyle</b> enumeration specifies the line style of a line drawn with a Windows GDI+ pen. The line can be drawn by using one of several predefined styles or a custom style.


## -enum-fields




### -field DashStyleSolid

Specifies a solid line. 


### -field DashStyleDash

Specifies a dashed line. 


### -field DashStyleDot

Specifies a dotted line. 


### -field DashStyleDashDot

Specifies an alternating dash-dot line. 


### -field DashStyleDashDotDot

Specifies an alternating dash-dot-dot line. 


### -field DashStyleCustom

Specifies a user-defined, custom dashed line. 


## -remarks



A custom dashed line is created by calling the 
				<a href="https://msdn.microsoft.com/library/ms535049(v=VS.85).aspx">Pen::SetDashPattern</a> method, which takes an array of values for the dash lengths and the space lengths.



