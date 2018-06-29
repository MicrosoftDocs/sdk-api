---
UID: NF:gdiplusbrush.HatchBrush.HatchBrush(IN HatchStyle,IN const Color &,IN const Color &)
title: HatchBrush::HatchBrush(IN HatchStyle,IN const Color &,IN const Color &)
author: windows-sdk-content
description: Creates a HatchBrush::HatchBrush object based on a hatch style, a foreground color, and a background color.
old-location: gdiplus\_gdiplus_CLASS_HatchBrush_HatchBrush_hatchStyle_foreColor_backColor_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\hatchbrushclass\hatchbrush_47hatchstyle_forecolor_backcolor.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: HatchBrush, HatchBrush class [GDI+],HatchBrush constructor, HatchBrush constructor [GDI+], HatchBrush constructor [GDI+],HatchBrush class, HatchBrush.HatchBrush, HatchBrush.HatchBrush(IN HatchStyle,IN const Color &,IN const Color &), HatchBrush::HatchBrush, HatchBrush::HatchBrush(IN HatchStyle,IN const Color &,IN const Color &), _gdiplus_CLASS_HatchBrush_HatchBrush_hatchStyle_foreColor_backColor_, gdiplus._gdiplus_CLASS_HatchBrush_HatchBrush_hatchStyle_foreColor_backColor_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusbrush.h
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
req.typenames: KnownGamingPrivileges
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - HatchBrush.HatchBrush
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# HatchBrush::HatchBrush(IN HatchStyle,IN const Color &,IN const Color &)


## -description


Creates a <b>HatchBrush::HatchBrush</b> object based on a hatch style, a foreground color, and a background color.


## -parameters




#### - hatchStyle [in]

Type: <b><a href="https://msdn.microsoft.com/library/ms534127(v=VS.85).aspx">HatchStyle</a></b>

Element of the <a href="https://msdn.microsoft.com/library/ms534127(v=VS.85).aspx">HatchStyle</a> enumeration that specifies the pattern of hatch lines that will be used. 


#### - foreColor [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a></b>

Reference to a color to use for the hatch lines. 


#### - backColor [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a></b>

Optional. Reference to a color to use for the background. The default value is <b>Color</b>()(a <a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> object created by the default <b>Color</b> constructor). 


## -see-also




<a href="https://msdn.microsoft.com/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/library/ms534459(v=VS.85).aspx">HatchBrush</a>



<a href="https://msdn.microsoft.com/library/ms534127(v=VS.85).aspx">HatchStyle</a>



<a href="https://msdn.microsoft.com/library/ms533811(v=VS.85).aspx">Using a Brush to Fill Shapes</a>
 

 

