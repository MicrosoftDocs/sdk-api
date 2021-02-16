---
UID: NF:gdiplusheaders.Region.Region(constBYTE,INT)
title: Region::Region(IN const BYTE,IN INT) (gdiplusheaders.h)
description: Creates a region that is defined by data obtained from another region.
helpviewer_keywords: ["Region","Region class [GDI+]","Region constructor","Region constructor [GDI+]","Region constructor [GDI+]","Region class","Region.Region","Region.Region(IN const BYTE","IN INT)","Region.Region(const BYTE*","INT)","Region::Region","Region::Region(IN const BYTE","IN INT)","_gdiplus_CLASS_Region_Region_regionData_size_","gdiplus._gdiplus_CLASS_Region_Region_regionData_size_"]
old-location: gdiplus\_gdiplus_CLASS_Region_Region_regionData_size_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\regionclass\regionconstructors\region_35regiondata_size.htm
ms.date: 12/05/2018
ms.keywords: Region, Region class [GDI+],Region constructor, Region constructor [GDI+], Region constructor [GDI+],Region class, Region.Region, Region.Region(IN const BYTE,IN INT), Region.Region(const BYTE*,INT), Region::Region, Region::Region(IN const BYTE,IN INT), _gdiplus_CLASS_Region_Region_regionData_size_, gdiplus._gdiplus_CLASS_Region_Region_regionData_size_
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
 - Region::Region
 - gdiplusheaders/Region::Region
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
 - Region.Region
---

# Region::Region(IN const BYTE,IN INT)


## -description

Creates a region that is defined by data obtained from another region.

## -parameters

### -param regionData [in]

Type: <b>const BYTE*</b>

Pointer to an array of bytes that specifies a region. The data contained in the bytes is obtained from another region by using the 
					<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-region-getdata">Region::GetData</a> method.

### -param size [in]

Type: <b>INT</b>

Integer that specifies the number of bytes in the 
					<i>regionData</i> array.