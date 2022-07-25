---
UID: NE:gdiplusenums.FlushIntention
title: FlushIntention (gdiplusenums.h)
description: The FlushIntention enumeration specifies when to flush the queue of graphics operations.
helpviewer_keywords: ["FlushIntention","FlushIntention enumeration [GDI+]","FlushIntentionFlush","FlushIntentionSync","_gdiplus_ENUM_FlushIntention","gdiplus._gdiplus_ENUM_FlushIntention","gdiplusenums/FlushIntention","gdiplusenums/FlushIntentionFlush","gdiplusenums/FlushIntentionSync"]
old-location: gdiplus\_gdiplus_ENUM_FlushIntention.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\flushintention.htm
ms.date: 12/05/2018
ms.keywords: FlushIntention, FlushIntention enumeration [GDI+], FlushIntentionFlush, FlushIntentionSync, _gdiplus_ENUM_FlushIntention, gdiplus._gdiplus_ENUM_FlushIntention, gdiplusenums/FlushIntention, gdiplusenums/FlushIntentionFlush, gdiplusenums/FlushIntentionSync
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - FlushIntention
 - gdiplusenums/FlushIntention
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - FlushIntention
---

# FlushIntention enumeration


## -description

The <b>FlushIntention</b> enumeration specifies when to flush the queue of graphics operations.

## -enum-fields

### -field FlushIntentionFlush:0

When passed to the 
				<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-flush">Graphics::Flush</a> method, specifies that pending rendering operations are executed as soon as possible. The 
				<b>Graphics::Flush</b> method is not synchronized with the completion of the rendering operations and might return before the rendering operations are completed.

### -field FlushIntentionSync

When passed to the 
				<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-flush">Graphics::Flush</a> method, specifies that pending rendering operations are executed as soon as possible. The 
				<b>Graphics::Flush</b> method is synchronized with the completion of the rendering operations; that is, it will not return until after the rendering operations are completed.
