---
UID: NF:winuser.OffsetRect
title: OffsetRect function
author: windows-sdk-content
description: The OffsetRect function moves the specified rectangle by the specified offsets.
old-location: gdi\offsetrect.htm
old-project: gdi
ms.assetid: 14101ad3-8c6e-459a-974a-1a8a4d8d7906
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: OffsetRect, OffsetRect function [Windows GDI], _win32_OffsetRect, gdi.offsetrect, winuser/OffsetRect
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
 - OffsetRect
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# OffsetRect function


## -description


The <b>OffsetRect</b> function moves the specified rectangle by the specified offsets.


## -parameters




### -param lprc [in, out]

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the logical coordinates of the rectangle to be moved.


### -param dx [in]

Specifies the amount to move the rectangle left or right. This parameter must be a negative value to move the rectangle to the left.


### -param dy [in]

Specifies the amount to move the rectangle up or down. This parameter must be a negative value to move the rectangle up.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



Because applications can use rectangles for different purposes, the rectangle functions do not use an explicit unit of measure. Instead, all rectangle coordinates and dimensions are given in signed, logical values. The mapping mode and the function in which the rectangle is used determine the units of measure.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/e8861240-9345-43e6-820d-d237247d1bd7">Using Rectangles</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9a52fb7f-cd35-4426-8753-c26cebef30d5">InflateRect</a>



<a href="https://msdn.microsoft.com/da686f78-e557-4ff2-9f24-b229f0c01563">IntersectRect</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/b03da8c9-ee6d-4045-8d90-8beceb09ead5">Rectangle Functions</a>



<a href="https://msdn.microsoft.com/23c251d1-b8c5-425f-b2b3-44954cf653e9">Rectangles Overview</a>



<a href="https://msdn.microsoft.com/f2da2df4-3f09-4c54-afd1-c728805f0f64">UnionRect</a>
 

 

