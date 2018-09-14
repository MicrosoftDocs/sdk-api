---
UID: NF:winuser.SubtractRect
title: SubtractRect function
author: windows-sdk-content
description: The SubtractRect function determines the coordinates of a rectangle formed by subtracting one rectangle from another.
old-location: gdi\subtractrect.htm
tech.root: gdi
ms.assetid: 85c8edae-af2b-4c6c-af37-2631e8b4edcd
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: SubtractRect, SubtractRect function [Windows GDI], _win32_SubtractRect, gdi.subtractrect, winuser/SubtractRect
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
 - SubtractRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SubtractRect function


## -description


The <b>SubtractRect</b> function determines the coordinates of a rectangle formed by subtracting one rectangle from another.


## -parameters




### -param lprcDst [out]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that receives the coordinates of the rectangle determined by subtracting the rectangle pointed to by <i>lprcSrc2</i> from the rectangle pointed to by <i>lprcSrc1</i>.


### -param lprcSrc1 [in]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure from which the function subtracts the rectangle pointed to by <i>lprcSrc2</i>.


### -param lprcSrc2 [in]

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that the function subtracts from the rectangle pointed to by <i>lprcSrc1</i>.


## -returns



If the resulting rectangle is empty, the return value is zero.

If the resulting rectangle is not empty, the return value is nonzero.




## -remarks



The function only subtracts the rectangle specified by <i>lprcSrc2</i> from the rectangle specified by <i>lprcSrc1</i> when the rectangles intersect completely in either the x- or y-direction. For example, if *<i>lprcSrc1</i> has the coordinates (10,10,100,100) and *<i>lprcSrc2</i> has the coordinates (50,50,150,150), the function sets the coordinates of the rectangle pointed to by <i>lprcDst</i> to (10,10,100,100). If *<i>lprcSrc1</i> has the coordinates (10,10,100,100) and *<i>lprcSrc2</i> has the coordinates (50,10,150,150), however, the function sets the coordinates of the rectangle pointed to by <i>lprcDst</i> to (10,10,50,100). In other words, the resulting rectangle is the bounding box of the geometric difference.

Because applications can use rectangles for different purposes, the rectangle functions do not use an explicit unit of measure. Instead, all rectangle coordinates and dimensions are given in signed, logical values. The mapping mode and the function in which the rectangle is used determine the units of measure.




## -see-also




<a href="https://msdn.microsoft.com/da686f78-e557-4ff2-9f24-b229f0c01563">IntersectRect</a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<a href="https://msdn.microsoft.com/b03da8c9-ee6d-4045-8d90-8beceb09ead5">Rectangle Functions</a>



<a href="https://msdn.microsoft.com/23c251d1-b8c5-425f-b2b3-44954cf653e9">Rectangles Overview</a>



<a href="https://msdn.microsoft.com/f2da2df4-3f09-4c54-afd1-c728805f0f64">UnionRect</a>
 

 

