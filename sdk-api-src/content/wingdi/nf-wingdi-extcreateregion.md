---
UID: NF:wingdi.ExtCreateRegion
title: ExtCreateRegion function
author: windows-sdk-content
description: The ExtCreateRegion function creates a region from the specified region and transformation data.
old-location: gdi\extcreateregion.htm
tech.root: gdi
ms.assetid: 4dcff824-eb1d-425c-b246-db4ace2c6518
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ExtCreateRegion, ExtCreateRegion function [Windows GDI], _win32_ExtCreateRegion, gdi.extcreateregion, wingdi/ExtCreateRegion
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-RTCore-GDI-rgn-l1-1-0.dll
 - api-ms-win-gdi-ie-rgn-l1-1-0.dll
 - ie_shims.dll
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
api_name:
 - ExtCreateRegion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ExtCreateRegion function


## -description


The <b>ExtCreateRegion</b> function creates a region from the specified region and transformation data.


## -parameters




### -param lpx [in]

A pointer to an <a href="https://msdn.microsoft.com/49f0d7ee-77fa-415e-af00-b8930253a3a9">XFORM</a> structure that defines the transformation to be performed on the region. If this pointer is <b>NULL</b>, the identity transformation is used.


### -param nCount [in]

The number of bytes pointed to by <i>lpRgnData</i>.


### -param lpData [in]

A pointer to a <a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a> structure that contains the region data in logical units.


## -returns



If the function succeeds, the return value is the value of the region.

If the function fails, the return value is <b>NULL</b>.




## -remarks



Region coordinates are represented as 27-bit signed integers.

An application can retrieve data for a region by calling the <a href="https://msdn.microsoft.com/e0d4862d-a405-4c00-b7b0-af4dd60407c0">GetRegionData</a> function.




## -see-also




<a href="https://msdn.microsoft.com/1113d3dc-8e3f-436c-a5a8-191785bc7fcc">CreatePolyPolygonRgn</a>



<a href="https://msdn.microsoft.com/dd7ad6de-c5f2-46e4-8d28-24caaa48ba3a">CreatePolygonRgn</a>



<a href="https://msdn.microsoft.com/17456440-c655-48ab-8d1e-ee770330f164">CreateRectRgn</a>



<a href="https://msdn.microsoft.com/f32e0b94-ce9c-4098-81fe-b239a9544621">CreateRectRgnIndirect</a>



<a href="https://msdn.microsoft.com/16f387e1-b00c-4755-8b21-1ee0f25bc46b">CreateRoundRectRgn</a>



<a href="https://msdn.microsoft.com/e0d4862d-a405-4c00-b7b0-af4dd60407c0">GetRegionData</a>



<a href="https://msdn.microsoft.com/3eac0b23-3138-4b34-9c16-6cc185e4de22">RGNDATA</a>



<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>



<a href="https://msdn.microsoft.com/49f0d7ee-77fa-415e-af00-b8930253a3a9">XFORM</a>
 

 

