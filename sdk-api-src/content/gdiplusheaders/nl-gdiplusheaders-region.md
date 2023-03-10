---
UID: NL:gdiplusheaders.Region
title: Region (gdiplusheaders.h)
description: The Region class describes an area of the display surface.
helpviewer_keywords: ["Region","Region class [GDI+]","Region class [GDI+]","described","_gdiplus_CLASS_Region_Class","gdiplus._gdiplus_CLASS_Region_Class","gdiplusheaders/Region"]
old-location: gdiplus\_gdiplus_CLASS_Region_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\region.htm
ms.date: 12/05/2018
ms.keywords: Region, Region class [GDI+], Region class [GDI+],described, _gdiplus_CLASS_Region_Class, gdiplus._gdiplus_CLASS_Region_Class, gdiplusheaders/Region
req.header: gdiplusheaders.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
ms.custom: 19H1
f1_keywords:
 - Region
 - gdiplusheaders/Region
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - Region
---

# Region class


## -description

The <b>Region</b> class describes an area of the display surface. The area can be any shape. In other words, the boundary of the area can be a combination of curved and straight lines. Regions can also be created from the interiors of rectangles, paths, or a combination of these. Regions are used in clipping and hit-testing operations.

## -remarks

A GDI+ region is stored in world coordinates whereas a GDI region is stored in device coordinates. Therefore, a GDI+ region is scalable and a GDI region is not. For more information, see the <b>Scalable Regions</b> section in <a href="/windows/desktop/gdiplus/-gdiplus-new-features-about">New Features</a>.

An application can use regions to clip the output of drawing operations. The Window Manager uses regions to define the drawing area of windows. These regions are called clipping regions. An application can also use regions in hit-testing operations, such as checking whether a point is in a region or whether a rectangle intersects a region. For more information, see <a href="/windows/desktop/gdiplus/-gdiplus-regions-about">Regions</a>, <a href="/windows/desktop/gdiplus/-gdiplus-clipping-about">Clipping</a>, and <a href="/windows/desktop/gdiplus/-gdiplus-using-regions-use">Using Regions</a>.