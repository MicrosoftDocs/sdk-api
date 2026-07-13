---
UID: NF:gdiplusheaders.Region.Equals
title: Region::Equals (gdiplusheaders.h)
description: The Region::Equals method determines whether this region is equal to a specified region.
helpviewer_keywords: ["Equals","Equals method [GDI+]","Equals method [GDI+]","Region class","Region class [GDI+]","Equals method","Region.Equals","Region::Equals","_gdiplus_CLASS_Region_Equals_region_g_","gdiplus._gdiplus_CLASS_Region_Equals_region_g_"]
old-location: gdiplus\_gdiplus_CLASS_Region_Equals_region_g_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\equals_59region_g.htm
ms.date: 12/05/2018
ms.keywords: Equals, Equals method [GDI+], Equals method [GDI+],Region class, Region class [GDI+],Equals method, Region.Equals, Region::Equals, _gdiplus_CLASS_Region_Equals_region_g_, gdiplus._gdiplus_CLASS_Region_Equals_region_g_
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
 - Region::Equals
 - gdiplusheaders/Region::Equals
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
 - Region.Equals
---

# Region::Equals


## -description

The <b>Region::Equals</b> method determines whether this region is equal to a specified region.

## -parameters

### -param region [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>*</b>

Pointer to a 
					<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a> object to test against this 
					<b>Region</b> object.

### -param g [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a> object that contains the world and page transformations required to calculate the device coordinates of this region and the region that is specified by the 
					<i>region</i> parameter.

## -returns

Type: <b>BOOL</b>

If this region is identical to the specified region, this method returns <b>TRUE</b>; otherwise, it returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics">Graphics</a>



<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>