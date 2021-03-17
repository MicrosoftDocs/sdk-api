---
UID: NF:gdiplusheaders.Region.IsInfinite
title: Region::IsInfinite (gdiplusheaders.h)
description: The Region::IsInfinite method determines whether this region is infinite.
helpviewer_keywords: ["IsInfinite","IsInfinite method [GDI+]","IsInfinite method [GDI+]","Region class","Region class [GDI+]","IsInfinite method","Region.IsInfinite","Region::IsInfinite","_gdiplus_CLASS_Region_IsInfinite_g_","gdiplus._gdiplus_CLASS_Region_IsInfinite_g_"]
old-location: gdiplus\_gdiplus_CLASS_Region_IsInfinite_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\isinfinite.htm
ms.date: 12/05/2018
ms.keywords: IsInfinite, IsInfinite method [GDI+], IsInfinite method [GDI+],Region class, Region class [GDI+],IsInfinite method, Region.IsInfinite, Region::IsInfinite, _gdiplus_CLASS_Region_IsInfinite_g_, gdiplus._gdiplus_CLASS_Region_IsInfinite_g_
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
 - Region::IsInfinite
 - gdiplusheaders/Region::IsInfinite
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
 - Region.IsInfinite
---

# Region::IsInfinite


## -description

The <b>Region::IsInfinite</b> method determines whether this region is infinite.

## -parameters

### -param g [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that contains the world and page transformations required to calculate the device coordinates of this region.

## -returns

Type: <b>BOOL</b>

If this region is infinite, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-region-isempty">Region::IsEmpty</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-region-makeempty">Region::MakeEmpty</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-region-makeinfinite">Region::MakeInfinite</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>