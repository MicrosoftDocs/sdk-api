---
UID: NF:wingdi.GetViewportOrgEx
title: GetViewportOrgEx function (wingdi.h)
description: The GetViewportOrgEx function retrieves the x-coordinates and y-coordinates of the viewport origin for the specified device context.
helpviewer_keywords: ["GetViewportOrgEx","GetViewportOrgEx function [Windows GDI]","_win32_GetViewportOrgEx","gdi.getviewportorgex","wingdi/GetViewportOrgEx"]
old-location: gdi\getviewportorgex.htm
tech.root: gdi
ms.assetid: 6e6c7090-edf4-46a3-8bcd-10a00c0cf847
ms.date: 12/05/2018
ms.keywords: GetViewportOrgEx, GetViewportOrgEx function [Windows GDI], _win32_GetViewportOrgEx, gdi.getviewportorgex, wingdi/GetViewportOrgEx
f1_keywords:
- wingdi/GetViewportOrgEx
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
- Ext-MS-Win-GDI-Draw-l1-1-1.dll
- ext-ms-win-gdi-draw-l1-1-2.dll
- Ext-MS-Win-GDI-Draw-L1-1-3.dll
- GDI32Full.dll
api_name:
- GetViewportOrgEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetViewportOrgEx function


## -description


The <b>GetViewportOrgEx</b> function retrieves the x-coordinates and y-coordinates of the viewport origin for the specified device context.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lppoint [out]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a> structure that receives the coordinates of the origin, in device units.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/coordinate-space-and-transformation-functions">Coordinate Space and Transformation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/coordinate-spaces-and-transformations">Coordinate Spaces and Transformations Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-getwindoworgex">GetWindowOrgEx</a>



<a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-setviewportorgex">SetViewportOrgEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-setwindoworgex">SetWindowOrgEx</a>
 

 

