---
UID: NF:wingdi.PolyBezierTo
title: PolyBezierTo function
author: windows-sdk-content
description: The PolyBezierTo function draws one or more B&#233;zier curves.
old-location: gdi\polybezierto.htm
tech.root: gdi
ms.assetid: 0c8d6d6d-d0a3-4188-91ad-934e6f054862
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: PolyBezierTo, PolyBezierTo function [Windows GDI], _win32_PolyBezierTo, gdi.polybezierto, wingdi/PolyBezierTo
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
 - Ext-MS-Win-GDI-Draw-l1-1-0.dll
 - Ext-MS-Win-GDI-Draw-l1-1-1.dll
 - ext-ms-win-gdi-draw-l1-1-2.dll
 - Ext-MS-Win-GDI-Draw-L1-1-3.dll
 - GDI32Full.dll
api_name:
 - PolyBezierTo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- PolyBezierTo
: 
---

# PolyBezierTo function


## -description


The <b>PolyBezierTo</b> function draws one or more Bézier curves.


## -parameters




### -param hdc [in]

A handle to a device context.


### -param apt [in]

A pointer to an array of <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structures that contains the endpoints and control points, in logical units.


### -param cpt [in]

The number of points in the <i>lppt</i> array. This value must be three times the number of curves to be drawn because each Bézier curve requires two control points and an ending point.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



This function draws cubic Bézier curves by using the control points specified by the <i>lppt</i> parameter. The first curve is drawn from the current position to the third point by using the first two points as control points. For each subsequent curve, the function needs exactly three more points, and uses the ending point of the previous curve as the starting point for the next.

<b>PolyBezierTo</b> moves the current position to the ending point of the last Bézier curve. The figure is not filled.

This function draws lines by using the current pen.




## -see-also




<a href="https://msdn.microsoft.com/90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b">Line and Curve Functions</a>



<a href="https://msdn.microsoft.com/8c65c185-8346-459e-bdf7-1cf3f7419736">Lines and Curves Overview</a>



<a href="https://msdn.microsoft.com/af11eeb7-4036-4a90-8685-9b5719f79e01">MoveToEx</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<a href="https://msdn.microsoft.com/d1622574-c65e-4265-9a17-22bb4d2cae0e">PolyBezier</a>
 

 

