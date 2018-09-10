---
UID: NF:wingdi.GetMapMode
title: GetMapMode function
author: windows-sdk-content
description: The GetMapMode function retrieves the current mapping mode.
old-location: gdi\getmapmode.htm
tech.root: gdi
ms.assetid: bc446b86-3dde-4460-bc54-1eaa4ad19941
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetMapMode, GetMapMode function [Windows GDI], _win32_GetMapMode, gdi.getmapmode, wingdi/GetMapMode
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
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - GetMapMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetMapMode function


## -description


The <b>GetMapMode</b> function retrieves the current mapping mode.


## -parameters




### -param hdc [in]

A handle to the device context.


## -returns



If the function succeeds, the return value specifies the mapping mode.

If the function fails, the return value is zero.




## -remarks



The following are the various mapping modes.

<table>
<tr>
<th>Mode</th>
<th>Description</th>
</tr>
<tr>
<td>MM_ANISOTROPIC</td>
<td>Logical units are mapped to arbitrary units with arbitrarily scaled axes. Use the <a href="https://msdn.microsoft.com/8fd13d56-f6fa-4aea-a7e5-535caf22a840">SetWindowExtEx</a> and <a href="https://msdn.microsoft.com/36bf82e0-f3e7-43cf-943f-eed783ad24a4">SetViewportExtEx</a> functions to specify the units, orientation, and scaling required.</td>
</tr>
<tr>
<td>MM_HIENGLISH</td>
<td>Each logical unit is mapped to 0.001 inch. Positive x is to the right; positive y is up.</td>
</tr>
<tr>
<td>MM_HIMETRIC</td>
<td>Each logical unit is mapped to 0.01 millimeter. Positive x is to the right; positive y is up.</td>
</tr>
<tr>
<td>MM_ISOTROPIC</td>
<td>Logical units are mapped to arbitrary units with equally scaled axes; that is, one unit along the x-axis is equal to one unit along the y-axis. Use the <a href="https://msdn.microsoft.com/8fd13d56-f6fa-4aea-a7e5-535caf22a840">SetWindowExtEx</a> and <a href="https://msdn.microsoft.com/36bf82e0-f3e7-43cf-943f-eed783ad24a4">SetViewportExtEx</a> functions to specify the units and the orientation of the axes. Graphics device interface makes adjustments as necessary to ensure the x and y units remain the same size. (When the windows extent is set, the viewport will be adjusted to keep the units isotropic).</td>
</tr>
<tr>
<td>MM_LOENGLISH</td>
<td>Each logical unit is mapped to 0.01 inch. Positive x is to the right; positive y is up.</td>
</tr>
<tr>
<td>MM_LOMETRIC</td>
<td>Each logical unit is mapped to 0.1 millimeter. Positive x is to the right; positive y is up.</td>
</tr>
<tr>
<td>MM_TEXT</td>
<td>Each logical unit is mapped to one device pixel. Positive x is to the right; positive y is down.</td>
</tr>
<tr>
<td>MM_TWIPS</td>
<td>Each logical unit is mapped to one twentieth of a printer's point (1/1440 inch, also called a "twip"). Positive x is to the right; positive y is up.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/a4d6a63a-6d2d-4bd9-9e71-4cd1b5f145a4">SetMapMode</a>



<a href="https://msdn.microsoft.com/36bf82e0-f3e7-43cf-943f-eed783ad24a4">SetViewportExtEx</a>



<a href="https://msdn.microsoft.com/8fd13d56-f6fa-4aea-a7e5-535caf22a840">SetWindowExtEx</a>
 

 

