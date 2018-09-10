---
UID: NF:wingdi.ScaleViewportExtEx
title: ScaleViewportExtEx function
author: windows-sdk-content
description: The ScaleViewportExtEx function modifies the viewport for a device context using the ratios formed by the specified multiplicands and divisors.
old-location: gdi\scaleviewportextex.htm
tech.root: gdi
ms.assetid: 8dde1322-82d7-4069-9655-a7bd3a324cb0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ScaleViewportExtEx, ScaleViewportExtEx function [Windows GDI], _win32_ScaleViewportExtEx, gdi.scaleviewportextex, wingdi/ScaleViewportExtEx
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
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - ScaleViewportExtEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ScaleViewportExtEx function


## -description


The <b>ScaleViewportExtEx</b> function modifies the viewport for a device context using the ratios formed by the specified multiplicands and divisors.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param xn [in]

The amount by which to multiply the current horizontal extent.


### -param dx [in]

The amount by which to divide the current horizontal extent.


### -param yn [in]

The amount by which to multiply the current vertical extent.


### -param yd [in]

The amount by which to divide the current vertical extent.


### -param lpsz [out]

A pointer to a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure that receives the previous viewport extents, in device units. If <i>lpSize</i> is <b>NULL</b>, this parameter is not used.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The viewport extents are modified as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
    xNewVE = (xOldVE * Xnum) / Xdenom 
    yNewVE = (yOldVE * Ynum) / Ydenom 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/e3fc188a-3796-497d-9d86-f116e9e48e30">GetViewportExtEx</a>



<a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a>
 

 

