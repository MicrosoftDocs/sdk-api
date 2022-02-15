---
UID: NF:gdiplusheaders.CachedBitmap.GetLastStatus
title: CachedBitmap::GetLastStatus (gdiplusheaders.h)
description: The CachedBitmap::GetLastStatus method returns a value that indicates whether this CachedBitmap object was constructed successfully.
helpviewer_keywords: ["CachedBitmap class [GDI+]","GetLastStatus method","CachedBitmap.GetLastStatus","CachedBitmap::GetLastStatus","GetLastStatus","GetLastStatus method [GDI+]","GetLastStatus method [GDI+]","CachedBitmap class","_gdiplus_CLASS_CachedBitmap_GetLastStatus_","gdiplus._gdiplus_CLASS_CachedBitmap_GetLastStatus_"]
old-location: gdiplus\_gdiplus_CLASS_CachedBitmap_GetLastStatus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\cachedbitmapclass\getlaststatus_27.htm
ms.date: 12/05/2018
ms.keywords: CachedBitmap class [GDI+],GetLastStatus method, CachedBitmap.GetLastStatus, CachedBitmap::GetLastStatus, GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],CachedBitmap class, _gdiplus_CLASS_CachedBitmap_GetLastStatus_, gdiplus._gdiplus_CLASS_CachedBitmap_GetLastStatus_
req.header: gdiplusheaders.h
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
 - CachedBitmap::GetLastStatus
 - gdiplusheaders/CachedBitmap::GetLastStatus
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
 - CachedBitmap.GetLastStatus
---

# CachedBitmap::GetLastStatus


## -description

The <b>CachedBitmap::GetLastStatus</b> method returns a value that indicates whether this 
			<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap">CachedBitmap</a> object was constructed successfully.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If this 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap">CachedBitmap</a> object was constructed successfully, the 
						<b>CachedBitmap::GetLastStatus</b> method returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If this 
						<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap">CachedBitmap</a> object was not constructed successfully, the <b>CachedBitmap::GetLastStatus</b> method returns an element of the 
						<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration that indicates the nature of the failure.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap">Bitmap</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-cachedbitmap">CachedBitmap</a>



<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image">Image</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-cached-bitmap-to-improve-performance-use">Using a Cached Bitmap to Improve Performance</a>
