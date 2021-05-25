---
UID: NF:gdiplusheaders.Region.Exclude(constGraphicsPath)
title: Region::Exclude(IN const GraphicsPath) (gdiplusheaders.h)
description: The Region::Exclude method updates this region to the portion of itself that does not intersect the specified path's interior.
helpviewer_keywords: ["Exclude","Exclude method [GDI+]","Exclude method [GDI+]","Region class","Region class [GDI+]","Exclude method","Region.Exclude","Region.Exclude(IN const GraphicsPath)","Region.Exclude(const GraphicsPath*)","Region::Exclude","Region::Exclude(IN const GraphicsPath)","_gdiplus_CLASS_Region_Exclude_path_","gdiplus._gdiplus_CLASS_Region_Exclude_path_"]
old-location: gdiplus\_gdiplus_CLASS_Region_Exclude_path_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionmethods\regionexcludemethods\exclude.htm
ms.date: 12/05/2018
ms.keywords: Exclude, Exclude method [GDI+], Exclude method [GDI+],Region class, Region class [GDI+],Exclude method, Region.Exclude, Region.Exclude(IN const GraphicsPath), Region.Exclude(const GraphicsPath*), Region::Exclude, Region::Exclude(IN const GraphicsPath), _gdiplus_CLASS_Region_Exclude_path_, gdiplus._gdiplus_CLASS_Region_Exclude_path_
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
 - Region::Exclude
 - gdiplusheaders/Region::Exclude
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
 - Region.Exclude
---

# Region::Exclude(IN const GraphicsPath)


## -description

The <b>Region::Exclude</b> method updates this region to the portion of itself that does not intersect the specified path's interior.

## -parameters

### -param path [in]

Type: <b>const <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>*</b>

Pointer to a <a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a> object that specifies the path to use to update this 
					<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a> object.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>, which is an element of the <b>Status</b> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath">GraphicsPath</a>



<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-region">Region</a>



<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>