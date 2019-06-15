---
UID: NF:gdiplusgraphics.Graphics.SetTextContrast
title: Graphics::SetTextContrast (gdiplusgraphics.h)
author: windows-sdk-content
description: The Graphics::SetTextContrast method sets the contrast value of this Graphics object. The contrast value is used for antialiasing text.
old-location: gdiplus\_gdiplus_CLASS_Graphics_SetTextContrast_contrast_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\settextcontrast.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Graphics class [GDI+],SetTextContrast method, Graphics.SetTextContrast, Graphics::SetTextContrast, SetTextContrast, SetTextContrast method [GDI+], SetTextContrast method [GDI+],Graphics class, _gdiplus_CLASS_Graphics_SetTextContrast_contrast_, gdiplus._gdiplus_CLASS_Graphics_SetTextContrast_contrast_
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
 - Graphics.SetTextContrast
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# Graphics::SetTextContrast


## -description


The <b>Graphics::SetTextContrast</b> method sets the contrast value of this <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object. The contrast value is used for antialiasing text. 


## -parameters




### -param contrast [in]

Type: <b>UINT</b>

<b>UINT</b> that specifies the contrast value for antialiasing text. 


## -returns



Type: <strong>Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.



