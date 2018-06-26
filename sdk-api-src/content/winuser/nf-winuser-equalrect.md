---
UID: NF:winuser.EqualRect
title: EqualRect function
author: windows-sdk-content
description: The EqualRect function determines whether the two specified rectangles are equal by comparing the coordinates of their upper-left and lower-right corners.
old-location: gdi\equalrect.htm
old-project: gdi
ms.assetid: 00763184-6b60-4095-b71e-5a851c2643aa
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: EqualRect, EqualRect function [Windows GDI], _win32_EqualRect, gdi.equalrect, winuser/EqualRect
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
req.typenames: POINTER_DEVICE_TYPE
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
 - EqualRect
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# EqualRect function


## -description


The <b>EqualRect</b> function determines whether the two specified rectangles are equal by comparing the coordinates of their upper-left and lower-right corners.


## -parameters




### -param lprc1 [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the logical coordinates of the first rectangle.


### -param lprc2 [in]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the logical coordinates of the second rectangle.


## -returns



If the two rectangles are identical, the return value is nonzero.

If the two rectangles are not identical, the return value is zero.




## -remarks



The <b>EqualRect</b> function does not treat empty rectangles as equal if their coordinates are different.

Because applications can use rectangles for different purposes, the rectangle functions do not use an explicit unit of measure. Instead, all rectangle coordinates and dimensions are given in signed, logical values. The mapping mode and the function in which the rectangle is used determine the units of measure.




## -see-also




<a href="https://msdn.microsoft.com/9deeed4f-304e-47a3-8259-ed7bc3815fd7">IsRectEmpty</a>



<a href="https://msdn.microsoft.com/8a47a238-082c-44b8-a270-5ebb4d3d9fc8">PtInRect</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/b03da8c9-ee6d-4045-8d90-8beceb09ead5">Rectangle Functions</a>



<a href="https://msdn.microsoft.com/23c251d1-b8c5-425f-b2b3-44954cf653e9">Rectangles Overview</a>
 

 

