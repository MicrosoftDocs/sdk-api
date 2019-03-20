---
UID: NF:winuser.PtInRect
title: PtInRect function (winuser.h)
author: windows-sdk-content
description: The PtInRect function determines whether the specified point lies within the specified rectangle.
old-location: gdi\ptinrect.htm
tech.root: gdi
ms.assetid: 8a47a238-082c-44b8-a270-5ebb4d3d9fc8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PtInRect, PtInRect function [Windows GDI], _win32_PtInRect, gdi.ptinrect, winuser/PtInRect
ms.topic: function
req.header: winuser.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - API-MS-Win-NTUser-Rectangle-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Rectangle-Ext-l1-1-0.dll
api_name:
 - PtInRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PtInRect function


## -description


The <b>PtInRect</b> function determines whether the specified point lies within the specified rectangle. A point is within a rectangle if it lies on the left or top side or is within all four sides. A point on the right or bottom side is considered outside the rectangle.


## -parameters




### -param lprc [in]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the specified rectangle.


### -param pt [in]

A <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that contains the specified point.


## -returns



If the specified point lies within the rectangle, the return value is nonzero.

If the specified point does not lie within the rectangle, the return value is zero.




## -remarks



The rectangle must be normalized before <b>PtInRect</b> is called. That is, lprc.right must be greater than lprc.left and lprc.bottom must be greater than lprc.top. If the rectangle is not normalized, a point is never considered inside of the rectangle.

Because applications can use rectangles for different purposes, the rectangle functions do not use an explicit unit of measure. Instead, all rectangle coordinates and dimensions are given in signed, logical values. The mapping mode and the function in which the rectangle is used determine the units of measure.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/e8861240-9345-43e6-820d-d237247d1bd7">Using Rectangles</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/00763184-6b60-4095-b71e-5a851c2643aa">EqualRect</a>



<a href="https://msdn.microsoft.com/9deeed4f-304e-47a3-8259-ed7bc3815fd7">IsRectEmpty</a>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<a href="https://msdn.microsoft.com/b03da8c9-ee6d-4045-8d90-8beceb09ead5">Rectangle Functions</a>



<a href="https://msdn.microsoft.com/23c251d1-b8c5-425f-b2b3-44954cf653e9">Rectangles Overview</a>
 

 

