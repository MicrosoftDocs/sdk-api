---
UID: NF:wingdi.SetViewportExtEx
title: SetViewportExtEx function
author: windows-sdk-content
description: Sets the horizontal and vertical extents of the viewport for a device context by using the specified values.
old-location: gdi\setviewportextex.htm
tech.root: gdi
ms.assetid: 36bf82e0-f3e7-43cf-943f-eed783ad24a4
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: SetViewportExtEx, SetViewportExtEx function [Windows GDI], _win32_SetViewportExtEx, gdi.setviewportextex, wingdi/SetViewportExtEx
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
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - SetViewportExtEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetViewportExtEx function


## -description


The <b>SetViewportExtEx</b> function sets the horizontal and vertical extents of the viewport for a device context by using the specified values.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param x [in]

The horizontal extent, in device units, of the viewport.


### -param y [in]

The vertical extent, in device units, of the viewport.


### -param lpsz [out]

A pointer to a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure that receives the previous viewport extents, in device units. If <i>lpSize</i> is <b>NULL</b>, this parameter is not used.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <i>viewport</i> refers to the device coordinate system of the device space. The <i>extent</i> is the maximum value of an axis. This function sets the maximum values for the horizontal and vertical axes of the viewport in device coordinates (or pixels). When mapping between page space and device space, <a href="https://msdn.microsoft.com/8fd13d56-f6fa-4aea-a7e5-535caf22a840">SetWindowExtEx</a> and <b>SetViewportExtEx</b> determine the scaling factor between the window and the viewport. For more information, see <a href="https://msdn.microsoft.com/1a232030-8561-4b57-b274-dca0a8b3e3a1">Transformation of Coordinate Spaces</a>.

When the following mapping modes are set, calls to the <a href="https://msdn.microsoft.com/8fd13d56-f6fa-4aea-a7e5-535caf22a840">SetWindowExtEx</a> and <b>SetViewportExtEx</b> functions are ignored.

<ul>
<li>MM_HIENGLISH</li>
<li>MM_HIMETRIC</li>
<li>MM_LOENGLISH</li>
<li>MM_LOMETRIC</li>
<li>MM_TEXT</li>
<li>MM_TWIPS</li>
</ul>
When MM_ISOTROPIC mode is set, an application must call the <a href="https://msdn.microsoft.com/8fd13d56-f6fa-4aea-a7e5-535caf22a840">SetWindowExtEx</a> function before it calls <b>SetViewportExtEx</b>. Note that for the MM_ISOTROPIC mode certain portions of a nonsquare screen may not be available for display because the logical units on both axes represent equal physical distances.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/41c2bc07-768b-4d27-a869-69b072f3e033">Invalidating the Client Area</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/e3fc188a-3796-497d-9d86-f116e9e48e30">GetViewportExtEx</a>



<a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a>



<a href="https://msdn.microsoft.com/8fd13d56-f6fa-4aea-a7e5-535caf22a840">SetWindowExtEx</a>
 

 

