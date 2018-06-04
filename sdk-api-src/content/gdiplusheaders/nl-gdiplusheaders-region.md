---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# Region class


## -description


The <b>Region</b> class describes an area of the display surface. The area can be any shape. In other words, the boundary of the area can be a combination of curved and straight lines. Regions can also be created from the interiors of rectangles, paths, or a combination of these. Regions are used in clipping and hit-testing operations.


## -remarks



A GDI+ region is stored in world coordinates whereas a GDI region is stored in device coordinates. Therefore, a GDI+ region is scalable and a GDI region is not. For more information, see the <b>Scalable Regions</b> section in <a href="https://msdn.microsoft.com/0257a23c-560e-472e-863a-6ab5881dc156">New Features</a>.

An application can use regions to clip the output of drawing operations. The Window Manager uses regions to define the drawing area of windows. These regions are called clipping regions. An application can also use regions in hit-testing operations, such as checking whether a point is in a region or whether a rectangle intersects a region. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn915768">Regions</a>, <a href="https://msdn.microsoft.com/58cc052d-31af-4410-81b9-defbad08a1dc">Clipping</a>, and <a href="https://msdn.microsoft.com/29a779c8-a2a4-42d8-9084-bad50ef82522">Using Regions</a>.



