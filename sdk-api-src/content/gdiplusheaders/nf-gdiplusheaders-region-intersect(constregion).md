---
UID: NF:gdiplusheaders.Region.Intersect(constRegion)
title: Region::Intersect(IN const Region) (gdiplusheaders.h)
description: The Region::Intersect method updates this region to the portion of itself that intersects another region.
helpviewer_keywords: ["Intersect","Intersect method [GDI+]","Intersect method [GDI+]","Region class","Region class [GDI+]","Intersect method","Region.Intersect","Region.Intersect(IN const Region)","Region.Intersect(const Region*)","Region::Intersect","Region::Intersect(IN const Region)","_gdiplus_CLASS_Region_Intersect_region_","gdiplus._gdiplus_CLASS_Region_Intersect_region_"]
old-location: gdiplus\_gdiplus_CLASS_Region_Intersect_region_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regionintersectmethods\intersect_48region.htm
ms.date: 12/05/2018
ms.keywords: Intersect, Intersect method [GDI+], Intersect method [GDI+],Region class, Region class [GDI+],Intersect method, Region.Intersect, Region.Intersect(IN const Region), Region.Intersect(const Region*), Region::Intersect, Region::Intersect(IN const Region), _gdiplus_CLASS_Region_Intersect_region_, gdiplus._gdiplus_CLASS_Region_Intersect_region_
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
 - Region::Intersect
 - gdiplusheaders/Region::Intersect
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
 - Region.Intersect
---

# Region::Intersect(IN const Region)


## -description

The <b>Region::Intersect</b> method updates this region to the portion of itself that intersects another region.

## -parameters

### -param region [in]

Type: <b>const <a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>*</b>

Pointer to a 
					<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a> object to use to update this 
					<b>Region</b> object.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rect">Rect</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>