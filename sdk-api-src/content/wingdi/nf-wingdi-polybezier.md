---
UID: NF:wingdi.PolyBezier
title: PolyBezier function
author: windows-sdk-content
description: The PolyBezier function draws one or more B&#233;zier curves.
old-location: gdi\polybezier.htm
tech.root: gdi
ms.assetid: d1622574-c65e-4265-9a17-22bb4d2cae0e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PolyBezier, PolyBezier function [Windows GDI], _win32_PolyBezier, gdi.polybezier, wingdi/PolyBezier
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
 - PolyBezier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- PolyBezier
: 
---

# PolyBezier function


## -description


The <b>PolyBezier</b> function draws one or more Bézier curves.


## -parameters




### -param hdc [in]

A handle to a device context.


### -param apt [in]

A pointer to an array of <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structures that contain the endpoints and control points of the curve(s), in logical units.


### -param cpt [in]

The number of points in the <i>lppt</i> array. This value must be one more than three times the number of curves to be drawn, because each Bézier curve requires two control points and an endpoint, and the initial curve requires an additional starting point.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



The <b>PolyBezier</b> function draws cubic Bézier curves by using the endpoints and control points specified by the <i>lppt</i> parameter. The first curve is drawn from the first point to the fourth point by using the second and third points as control points. Each subsequent curve in the sequence needs exactly three more points: the ending point of the previous curve is used as the starting point, the next two points in the sequence are control points, and the third is the ending point.

The current position is neither used nor updated by the <b>PolyBezier</b> function. The figure is not filled.

This function draws lines by using the current pen.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/3407014d-6427-45e9-8be4-b8037ca5438f">Redrawing in the Update Region</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/90f123e2-c3c7-4ba1-a42b-7d6bc0074d5b">Line and Curve Functions</a>



<a href="https://msdn.microsoft.com/8c65c185-8346-459e-bdf7-1cf3f7419736">Lines and Curves Overview</a>



<a href="https://msdn.microsoft.com/af11eeb7-4036-4a90-8685-9b5719f79e01">MoveToEx</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<a href="https://msdn.microsoft.com/0c8d6d6d-d0a3-4188-91ad-934e6f054862">PolyBezierTo</a>
 

 

