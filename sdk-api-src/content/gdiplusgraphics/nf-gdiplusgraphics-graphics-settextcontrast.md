---
UID: NF:gdiplusgraphics.Graphics.SetTextContrast
title: Graphics::SetTextContrast
author: windows-sdk-content
description: The Graphics::SetTextContrast method sets the contrast value of this Graphics object. The contrast value is used for antialiasing text.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetTextContrast_contrast_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\settextcontrast.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Graphics class [GDI+],SetTextContrast method, Graphics.SetTextContrast, Graphics::SetTextContrast, SetTextContrast, SetTextContrast method [GDI+], SetTextContrast method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetTextContrast_contrast_, gdiplus._gdiplus_CLASS_Graphics_SetTextContrast_contrast_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gdiplusgraphics.h
req.include-header: Gdiplus.h
req.redist: 
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
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Graphics.SetTextContrast
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# Graphics::SetTextContrast


## -description


The <b>Graphics::SetTextContrast</b> method sets the contrast value of this <a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a> object. The contrast value is used for antialiasing text. 


## -parameters




### -param contrast [in]

Type: <b>UINT</b>

<b>UINT</b> that specifies the contrast value for antialiasing text. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.



