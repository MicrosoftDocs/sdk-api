---
UID: NF:wingdi.CreateRoundRectRgn
title: CreateRoundRectRgn function (wingdi.h)
author: windows-sdk-content
description: The CreateRoundRectRgn function creates a rectangular region with rounded corners.
old-location: gdi\createroundrectrgn.htm
tech.root: gdi
ms.assetid: 16f387e1-b00c-4755-8b21-1ee0f25bc46b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateRoundRectRgn, CreateRoundRectRgn function [Windows GDI], _win32_CreateRoundRectRgn, gdi.createroundrectrgn, wingdi/CreateRoundRectRgn
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
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
 - API-MS-Win-GDI-Internal-Uap-L1-1-0.dll
 - GDI32Full.dll
 - GDI32Min.dll
api_name:
 - CreateRoundRectRgn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateRoundRectRgn function


## -description


The <b>CreateRoundRectRgn</b> function creates a rectangular region with rounded corners.


## -parameters




### -param x1 [in]

Specifies the x-coordinate of the upper-left corner of the region in device units.


### -param y1 [in]

Specifies the y-coordinate of the upper-left corner of the region in device units.


### -param x2 [in]

Specifies the x-coordinate of the lower-right corner of the region in device units.


### -param y2 [in]

Specifies the y-coordinate of the lower-right corner of the region in device units.


### -param w [in]

Specifies the width of the ellipse used to create the rounded corners in device units.


### -param h [in]

Specifies the height of the ellipse used to create the rounded corners in device units.


## -returns



If the function succeeds, the return value is the handle to the region.

If the function fails, the return value is <b>NULL</b>.




## -remarks



When you no longer need the <b>HRGN</b> object call the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete it.

Region coordinates are represented as 27-bit signed  integers.




## -see-also




<a href="https://msdn.microsoft.com/1113d3dc-8e3f-436c-a5a8-191785bc7fcc">CreatePolyPolygonRgn</a>



<a href="https://msdn.microsoft.com/dd7ad6de-c5f2-46e4-8d28-24caaa48ba3a">CreatePolygonRgn</a>



<a href="https://msdn.microsoft.com/17456440-c655-48ab-8d1e-ee770330f164">CreateRectRgn</a>



<a href="https://msdn.microsoft.com/f32e0b94-ce9c-4098-81fe-b239a9544621">CreateRectRgnIndirect</a>



<a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>



<a href="https://msdn.microsoft.com/4dcff824-eb1d-425c-b246-db4ace2c6518">ExtCreateRegion</a>



<a href="https://msdn.microsoft.com/e0d4862d-a405-4c00-b7b0-af4dd60407c0">GetRegionData</a>



<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>



<a href="https://msdn.microsoft.com/a89b875e-923d-4048-bc61-8dea132cc56d">SelectObject</a>
 

 

