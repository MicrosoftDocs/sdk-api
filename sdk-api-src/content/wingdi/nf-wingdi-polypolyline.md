---
UID: NF:wingdi.PolyPolyline
title: PolyPolyline function
author: windows-sdk-content
description: The PolyPolyline function draws multiple series of connected line segments.
old-location: gdi\polypolyline.htm
old-project: gdi
ms.assetid: 71a9273f-321b-4efb-ac73-5979f8151d05
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PolyPolyline, PolyPolyline function [Windows GDI], _win32_PolyPolyline, gdi.polypolyline, wingdi/PolyPolyline
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: DISPLAYCONFIG_VIDEO_OUTPUT_TECHNOLOGY
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
 - PolyPolyline
product: Windows
targetos: Windows
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PolyPolyline function


## -description


The <b>PolyPolyline</b> function draws multiple series of connected line segments.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param apt [in]

A pointer to an array of <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structures that contains the vertices of the polylines, in logical units. The polylines are specified consecutively.


### -param asz [in]

A pointer to an array of variables specifying the number of points in the <i>lppt</i> array for the corresponding polyline. Each entry must be greater than or equal to two.


### -param csz [in]

The total number of entries in the <i>lpdwPolyPoints</i> array.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The line segments are drawn by using the current pen. The figures formed by the segments are not filled.

The current position is neither used nor updated by this function.




## -see-also




<a href="https://msdn.microsoft.com/90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b">Line and Curve Functions</a>



<a href="https://msdn.microsoft.com/8c65c185-8346-459e-bdf7-1cf3f7419736">Lines and Curves Overview</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<a href="https://msdn.microsoft.com/55481dd0-3db7-4131-b383-4d0036943e60">Polyline</a>



<a href="https://msdn.microsoft.com/76020742-b651-4244-82c3-13034573c306">PolylineTo</a>
 

 

