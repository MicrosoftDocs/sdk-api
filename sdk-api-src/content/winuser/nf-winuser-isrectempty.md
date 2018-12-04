---
UID: NF:winuser.IsRectEmpty
title: IsRectEmpty function
author: windows-sdk-content
description: The IsRectEmpty function determines whether the specified rectangle is empty.
old-location: gdi\isrectempty.htm
tech.root: gdi
ms.assetid: 9deeed4f-304e-47a3-8259-ed7bc3815fd7
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IsRectEmpty, IsRectEmpty function [Windows GDI], _win32_IsRectEmpty, gdi.isrectempty, winuser/IsRectEmpty
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
 - IsRectEmpty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsRectEmpty function


## -description


The <b>IsRectEmpty</b> function determines whether the specified rectangle is empty. An empty rectangle is one that has no area; that is, the coordinate of the right side is less than or equal to the coordinate of the left side, or the coordinate of the bottom side is less than or equal to the coordinate of the top side.


## -parameters




### -param lprc [in]

Pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the logical coordinates of the rectangle.


## -returns



If the rectangle is empty, the return value is nonzero.

If the rectangle is not empty, the return value is zero.




## -remarks



Because applications can use rectangles for different purposes, the rectangle functions do not use an explicit unit of measure. Instead, all rectangle coordinates and dimensions are given in signed, logical values. The mapping mode and the function in which the rectangle is used determine the units of measure.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/e8861240-9345-43e6-820d-d237247d1bd7">Using Rectangles</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/00763184-6b60-4095-b71e-5a851c2643aa">EqualRect</a>



<a href="https://msdn.microsoft.com/8a47a238-082c-44b8-a270-5ebb4d3d9fc8">PtInRect</a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<a href="https://msdn.microsoft.com/b03da8c9-ee6d-4045-8d90-8beceb09ead5">Rectangle Functions</a>



<a href="https://msdn.microsoft.com/23c251d1-b8c5-425f-b2b3-44954cf653e9">Rectangles Overview</a>
 

 

