---
UID: NL:gdiplusheaders.Region
title: Region
author: windows-sdk-content
description: The Region class describes an area of the display surface.
old-location: gdiplus\_gdiplus_CLASS_Region_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\region.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: Region, Region class [GDI+], Region class [GDI+],described, _gdiplus_CLASS_Region_Class, gdiplus._gdiplus_CLASS_Region_Class, gdiplusheaders/Region
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdiplusheaders.h
api_name:
 - Region
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Region class


## -description


The <b>Region</b> class describes an area of the display surface. The area can be any shape. In other words, the boundary of the area can be a combination of curved and straight lines. Regions can also be created from the interiors of rectangles, paths, or a combination of these. Regions are used in clipping and hit-testing operations.


## -remarks



A GDI+ region is stored in world coordinates whereas a GDI region is stored in device coordinates. Therefore, a GDI+ region is scalable and a GDI region is not. For more information, see the <b>Scalable Regions</b> section in <a href="https://msdn.microsoft.com/en-us/library/ms536340(v=VS.85).aspx">New Features</a>.

An application can use regions to clip the output of drawing operations. The Window Manager uses regions to define the drawing area of windows. These regions are called clipping regions. An application can also use regions in hit-testing operations, such as checking whether a point is in a region or whether a rectangle intersects a region. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms536378(v=VS.85).aspx">Regions</a>, <a href="https://msdn.microsoft.com/en-us/library/ms536360(v=VS.85).aspx">Clipping</a>, and <a href="https://msdn.microsoft.com/en-us/library/ms533816(v=VS.85).aspx">Using Regions</a>.



