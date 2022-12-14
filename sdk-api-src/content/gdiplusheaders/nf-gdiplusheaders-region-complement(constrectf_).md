---
UID: NF:gdiplusheaders.Region.Complement(constRectF&)
title: Region::Complement(IN const RectF &) (gdiplusheaders.h)
description: The Region::Complement method updates this region to the portion of the specified rectangle's interior that does not intersect this region.
helpviewer_keywords: ["Complement","Complement method [GDI+]","Complement method [GDI+]","Region class","Region class [GDI+]","Complement method","Region.Complement","Region.Complement(IN const RectF &)","Region.Complement(const RectF&)","Region::Complement","Region::Complement(IN const RectF &)","_gdiplus_CLASS_Region_Complement_RectF_rect_","gdiplus._gdiplus_CLASS_Region_Complement_RectF_rect_"]
old-location: gdiplus\_gdiplus_CLASS_Region_Complement_RectF_rect_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regioncomplementmethods\complement_78rectfamprect.htm
ms.date: 12/05/2018
ms.keywords: Complement, Complement method [GDI+], Complement method [GDI+],Region class, Region class [GDI+],Complement method, Region.Complement, Region.Complement(IN const RectF &), Region.Complement(const RectF&), Region::Complement, Region::Complement(IN const RectF &), _gdiplus_CLASS_Region_Complement_RectF_rect_, gdiplus._gdiplus_CLASS_Region_Complement_RectF_rect_
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
 - Region::Complement
 - gdiplusheaders/Region::Complement
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
 - Region.Complement
---

# Region::Complement(IN const RectF &)


## -description

The <b>Region::Complement</b> method updates this region to the portion of the specified rectangle's interior that does not intersect this region.

## -parameters

### -param rect [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a></b>

Reference to a rectangle to use to update this 
					<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a> object.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-rectf">RectF</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>