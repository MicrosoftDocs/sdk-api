---
UID: NE:gdiplusenums.FlushIntention
title: FlushIntention
author: windows-sdk-content
description: The FlushIntention enumeration specifies when to flush the queue of graphics operations.
old-location: gdiplus\_gdiplus_ENUM_FlushIntention.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\flushintention.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: FlushIntention, FlushIntention enumeration [GDI+], FlushIntentionFlush, FlushIntentionSync, _gdiplus_ENUM_FlushIntention, gdiplus._gdiplus_ENUM_FlushIntention, gdiplusenums/FlushIntention, gdiplusenums/FlushIntentionFlush, gdiplusenums/FlushIntentionSync
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
 - FlushIntention
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# FlushIntention enumeration


## -description


The <b>FlushIntention</b> enumeration specifies when to flush the queue of graphics operations.


## -enum-fields




### -field FlushIntentionFlush

When passed to the 
				<a href="https://msdn.microsoft.com/en-us/library/ms535692(v=VS.85).aspx">Graphics::Flush</a> method, specifies that pending rendering operations are executed as soon as possible. The 
				<b>Graphics::Flush</b> method is not synchronized with the completion of the rendering operations and might return before the rendering operations are completed. 


### -field FlushIntentionSync

When passed to the 
				<a href="https://msdn.microsoft.com/en-us/library/ms535692(v=VS.85).aspx">Graphics::Flush</a> method, specifies that pending rendering operations are executed as soon as possible. The 
				<b>Graphics::Flush</b> method is synchronized with the completion of the rendering operations; that is, it will not return until after the rendering operations are completed. 

