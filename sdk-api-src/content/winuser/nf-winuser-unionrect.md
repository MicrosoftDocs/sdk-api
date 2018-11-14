---
UID: NF:winuser.UnionRect
title: UnionRect function
author: windows-sdk-content
description: The UnionRect function creates the union of two rectangles. The union is the smallest rectangle that contains both source rectangles.
old-location: gdi\unionrect.htm
tech.root: gdi
ms.assetid: f2da2df4-3f09-4c54-afd1-c728805f0f64
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: UnionRect, UnionRect function [Windows GDI], _win32_UnionRect, gdi.unionrect, winuser/UnionRect
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - UnionRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- UnionRect
: 
---

# UnionRect function


## -description


The <b>UnionRect</b> function creates the union of two rectangles. The union is the smallest rectangle that contains both source rectangles.


## -parameters




### -param lprcDst [out]

A pointer to the <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that will receive a rectangle containing the rectangles pointed to by the <i>lprcSrc1</i> and <i>lprcSrc2</i> parameters.


### -param lprcSrc1 [in]

A pointer to the <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the first source rectangle.


### -param lprcSrc2 [in]

A pointer to the <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the second source rectangle.


## -returns



If the specified structure contains a nonempty rectangle, the return value is nonzero.

If the specified structure does not contain a nonempty rectangle, the return value is zero.




## -remarks



The system ignores the dimensions of an empty rectangle that is, a rectangle in which all coordinates are set to zero, so that it has no height or no width.

Because applications can use rectangles for different purposes, the rectangle functions do not use an explicit unit of measure. Instead, all rectangle coordinates and dimensions are given in signed, logical values. The mapping mode and the function in which the rectangle is used determine the units of measure.




## -see-also




<a href="https://msdn.microsoft.com/9a52fb7f-cd35-4426-8753-c26cebef30d5">InflateRect</a>



<a href="https://msdn.microsoft.com/da686f78-e557-4ff2-9f24-b229f0c01563">IntersectRect</a>



<a href="https://msdn.microsoft.com/14101ad3-8c6e-459a-974a-1a8a4d8d7906">OffsetRect</a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<a href="https://msdn.microsoft.com/b03da8c9-ee6d-4045-8d90-8beceb09ead5">Rectangle Functions</a>



<a href="https://msdn.microsoft.com/23c251d1-b8c5-425f-b2b3-44954cf653e9">Rectangles Overview</a>
 

 

