---
UID: NF:wingdi.DPtoLP
title: DPtoLP function
author: windows-driver-content
description: The DPtoLP function converts device coordinates into logical coordinates. The conversion depends on the mapping mode of the device context, the settings of the origins and extents for the window and viewport, and the world transformation.
old-location: gdi\dptolp.htm
old-project: gdi
ms.assetid: 0106867c-e8c5-4826-8cba-60c29e1d021a
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: DPtoLP, DPtoLP function [Windows GDI], _win32_DPtoLP, gdi.dptolp, wingdi/DPtoLP
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
-	DPtoLP
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# DPtoLP function


## -description


The <b>DPtoLP</b> function converts device coordinates into logical coordinates. The conversion depends on the mapping mode of the device context, the settings of the origins and extents for the window and viewport, and the world transformation.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lppt

TBD


### -param c

TBD




#### - lpPoints [in, out]

A pointer to an array of <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structures. The x- and y-coordinates contained in each <b>POINT</b> structure will be transformed.


#### - nCount [in]

The number of points in the array.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>DPtoLP</b> function fails if the device coordinates exceed 27 bits, or if the converted logical coordinates exceed 32 bits. In the case of such an overflow, the results for all the points are undefined.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/61db38d7-9371-4ff1-b96b-1bed4c2a2749">Using Coordinate Spaces and Transformations</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3ebcabf2-9718-47b2-aba0-7cc28fa42e5a">Coordinate Space and Transformation Functions</a>



<a href="https://msdn.microsoft.com/cfb02788-9b73-4451-9e68-2ad310e0e527">Coordinate Spaces and Transformations Overview</a>



<a href="https://msdn.microsoft.com/670a16fb-842e-4250-9ad7-dc08e849c2ba">LPtoDP</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a>
 

 

