---
UID: NF:winuser.IntersectRect
title: IntersectRect function
author: windows-sdk-content
description: The IntersectRect function calculates the intersection of two source rectangles and places the coordinates of the intersection rectangle into the destination rectangle.
old-location: gdi\intersectrect.htm
old-project: gdi
ms.assetid: da686f78-e557-4ff2-9f24-b229f0c01563
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IntersectRect, IntersectRect function [Windows GDI], _win32_IntersectRect, gdi.intersectrect, winuser/IntersectRect
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
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
 - IntersectRect
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IntersectRect function


## -description


The <b>IntersectRect</b> function calculates the intersection of two source rectangles and places the coordinates of the intersection rectangle into the destination rectangle. If the source rectangles do not intersect, an empty rectangle (in which all coordinates are set to zero) is placed into the destination rectangle.


## -parameters




### -param lprcDst [out]

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that is to receive the intersection of the rectangles pointed to by the <i>lprcSrc1</i> and <i>lprcSrc2</i> parameters. This parameter cannot be <b>NULL</b>.


### -param lprcSrc1 [in]

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the first source rectangle.


### -param lprcSrc2 [in]

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the second source rectangle.


## -returns



If the rectangles intersect, the return value is nonzero.

If the rectangles do not intersect, the return value is zero.




## -remarks



Because applications can use rectangles for different purposes, the rectangle functions do not use an explicit unit of measure. Instead, all rectangle coordinates and dimensions are given in signed, logical values. The mapping mode and the function in which the rectangle is used determine the units of measure.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/e8861240-9345-43e6-820d-d237247d1bd7">Using Rectangles</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9a52fb7f-cd35-4426-8753-c26cebef30d5">InflateRect</a>



<a href="https://msdn.microsoft.com/14101ad3-8c6e-459a-974a-1a8a4d8d7906">OffsetRect</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/b03da8c9-ee6d-4045-8d90-8beceb09ead5">Rectangle Functions</a>



<a href="https://msdn.microsoft.com/23c251d1-b8c5-425f-b2b3-44954cf653e9">Rectangles Overview</a>



<a href="https://msdn.microsoft.com/f2da2df4-3f09-4c54-afd1-c728805f0f64">UnionRect</a>
 

 

