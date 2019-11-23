---
UID: NF:wingdi.CreateRectRgnIndirect
title: CreateRectRgnIndirect function (wingdi.h)

description: The CreateRectRgnIndirect function creates a rectangular region.
old-location: gdi\createrectrgnindirect.htm
tech.root: gdi
ms.assetid: f32e0b94-ce9c-4098-81fe-b239a9544621

ms.date: 12/05/2018
ms.keywords: CreateRectRgnIndirect, CreateRectRgnIndirect function [Windows GDI], _win32_CreateRectRgnIndirect, gdi.createrectrgnindirect, wingdi/CreateRectRgnIndirect
ms.topic: function
f1_keywords: 
 - "wingdi/CreateRectRgnIndirect"
dev_langs:
 - c++
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
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
api_name:
 - CreateRectRgnIndirect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreateRectRgnIndirect function


## -description


The <b>CreateRectRgnIndirect</b> function creates a rectangular region.


## -parameters




### -param lprect [in]

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that contains the coordinates of the upper-left and lower-right corners of the rectangle that defines the region in logical units.


## -returns



If the function succeeds, the return value is the handle to the region.

If the function fails, the return value is <b>NULL</b>.




## -remarks



When you no longer need the <b>HRGN</b> object, call the <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a> function to delete it.

Region coordinates are represented as 27-bit signed integers.

The region will be exclusive of the bottom and right edges.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-createpolypolygonrgn">CreatePolyPolygonRgn</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-createpolygonrgn">CreatePolygonRgn</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-createrectrgn">CreateRectRgn</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-createroundrectrgn">CreateRoundRectRgn</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-deleteobject">DeleteObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-extcreateregion">ExtCreateRegion</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getregiondata">GetRegionData</a>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/region-functions">Region Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/regions">Regions Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-selectobject">SelectObject</a>
 

 

