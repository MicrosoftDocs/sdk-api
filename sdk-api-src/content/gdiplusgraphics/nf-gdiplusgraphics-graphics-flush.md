---
UID: NF:gdiplusgraphics.Graphics.Flush
title: Graphics::Flush (gdiplusgraphics.h)
description: The Graphics::Flush method flushes all pending graphics operations.
helpviewer_keywords: ["Flush","Flush method [GDI+]","Flush method [GDI+]","Graphics class","Graphics class [GDI+]","Flush method","Graphics.Flush","Graphics::Flush","_gdiplus_CLASS_Graphics_Flush_intention_","gdiplus._gdiplus_CLASS_Graphics_Flush_intention_"]
old-location: gdiplus\_gdiplus_CLASS_Graphics_Flush_intention_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicsclass\graphicsmethods\flush.htm
ms.date: 12/05/2018
ms.keywords: Flush, Flush method [GDI+], Flush method [GDI+],Graphics class, Graphics class [GDI+],Flush method, Graphics.Flush, Graphics::Flush, _gdiplus_CLASS_Graphics_Flush_intention_, gdiplus._gdiplus_CLASS_Graphics_Flush_intention_
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Graphics::Flush
 - gdiplusgraphics/Graphics::Flush
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Graphics.Flush
---

# Graphics::Flush


## -description

The <b>Graphics::Flush</b> method flushes all pending graphics operations.

## -parameters

### -param intention [in]

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-flushintention">FlushIntention</a></b>

Element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-flushintention">FlushIntention</a> enumeration that specifies whether pending operations are flushed immediately (not executed) or executed as soon as possible.

## -see-also

<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-flushintention">FlushIntention</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>