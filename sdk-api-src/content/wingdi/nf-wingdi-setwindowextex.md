---
UID: NF:wingdi.SetWindowExtEx
title: SetWindowExtEx function
author: windows-sdk-content
description: The SetWindowExtEx function sets the horizontal and vertical extents of the window for a device context by using the specified values.
old-location: gdi\setwindowextex.htm
old-project: gdi
ms.assetid: 8fd13d56-f6fa-4aea-a7e5-535caf22a840
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SetWindowExtEx, SetWindowExtEx function [Windows GDI], _win32_SetWindowExtEx, gdi.setwindowextex, wingdi/SetWindowExtEx
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	gdi32.dll
-	Ext-MS-Win-GDI-Draw-l1-1-1.dll
-	ext-ms-win-gdi-draw-l1-1-2.dll
-	Ext-MS-Win-GDI-Draw-L1-1-3.dll
-	GDI32Full.dll
api_name:
-	SetWindowExtEx
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetWindowExtEx function


## -description


The <b>SetWindowExtEx</b> function sets the horizontal and vertical extents of the window for a device context by using the specified values.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param x

TBD


### -param y

TBD


### -param lpsz

TBD




#### - lpSize [out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure that receives the previous window extents, in logical units. If <i>lpSize</i> is <b>NULL</b>, this parameter is not used.


#### - nXExtent [in]

The window's horizontal extent in logical units.


#### - nYExtent [in]

The window's vertical extent in logical units.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <i>window</i> refers to the logical coordinate system of the page space. The <i>extent</i> is the maximum value of an axis. This function sets the maximum values for the horizontal and vertical axes of the window (in logical coordinates). When mapping between page space and device space, <a href="https://msdn.microsoft.com/36bf82e0-f3e7-43cf-943f-eed783ad24a4">SetViewportExtEx</a> and <b>SetWindowExtEx</b> determine the scaling factor between the window and the viewport. For more information, see <a href="https://msdn.microsoft.com/1a232030-8561-4b57-b274-dca0a8b3e3a1">Transformation of Coordinate Spaces</a>.

When the following mapping modes are set, calls to the <b>SetWindowExtEx</b> and <a href="https://msdn.microsoft.com/36bf82e0-f3e7-43cf-943f-eed783ad24a4">SetViewportExtEx</a> functions are ignored:

<ul>
<li>MM_HIENGLISH</li>
<li>MM_HIMETRIC</li>
<li>MM_LOENGLISH</li>
<li>MM_LOMETRIC</li>
<li>MM_TEXT</li>
<li>MM_TWIPS</li>
</ul>
When MM_ISOTROPIC mode is set, an application must call the <b>SetWindowExtEx</b> function before calling <a href="https://msdn.microsoft.com/36bf82e0-f3e7-43cf-943f-eed783ad24a4">SetViewportExtEx</a>. Note that for the MM_ISOTROPIC mode, certain portions of a nonsquare screen may not be available for display because the logical units on both axes represent equal physical distances.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/41c2bc07-768b-4d27-a869-69b072f3e033">Invalidating the Client Area</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/17f41fcb-c9a4-4b7e-acde-73450044413e">GetWindowExtEx</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a>



<a href="https://msdn.microsoft.com/36bf82e0-f3e7-43cf-943f-eed783ad24a4">SetViewportExtEx</a>
 

 

