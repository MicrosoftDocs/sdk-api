---
UID: NF:winuser.InflateRect
title: InflateRect function
author: windows-driver-content
description: The InflateRect function increases or decreases the width and height of the specified rectangle.
old-location: gdi\inflaterect.htm
old-project: gdi
ms.assetid: 9a52fb7f-cd35-4426-8753-c26cebef30d5
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: InflateRect, InflateRect function [Windows GDI], _win32_InflateRect, gdi.inflaterect, winuser/InflateRect
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
req.typenames: AR_STATE, *PAR_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	user32.dll
-	API-MS-Win-NTUser-Rectangle-l1-1-0.dll
-	minuser.dll
-	Ext-MS-Win-NTUser-Rectangle-Ext-l1-1-0.dll
api_name:
-	InflateRect
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# InflateRect function


## -description


The <b>InflateRect</b> function increases or decreases the width and height of the specified rectangle. The <b>InflateRect</b> function adds <i>dx</i> units to the left and right ends of the rectangle and <i>dy</i> units to the top and bottom. The <i>dx</i> and <i>dy</i> parameters are signed values; positive values increase the width and height, and negative values decrease them.


## -parameters




### -param lprc [in, out]

A pointer to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that increases or decreases in size.


### -param dx [in]

The amount to increase or decrease the rectangle width. This parameter must be negative to decrease the width.


### -param dy [in]

The amount to increase or decrease the rectangle height. This parameter must be negative to decrease the height.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



Because applications can use rectangles for different purposes, the rectangle functions do not use an explicit unit of measure. Instead, all rectangle coordinates and dimensions are given in signed, logical values. The mapping mode and the function in which the rectangle is used determine the units of measure.




## -see-also




<a href="https://msdn.microsoft.com/da686f78-e557-4ff2-9f24-b229f0c01563">IntersectRect</a>



<a href="https://msdn.microsoft.com/14101ad3-8c6e-459a-974a-1a8a4d8d7906">OffsetRect</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<a href="https://msdn.microsoft.com/b03da8c9-ee6d-4045-8d90-8beceb09ead5">Rectangle Functions</a>



<a href="https://msdn.microsoft.com/23c251d1-b8c5-425f-b2b3-44954cf653e9">Rectangles Overview</a>



<a href="https://msdn.microsoft.com/f2da2df4-3f09-4c54-afd1-c728805f0f64">UnionRect</a>
 

 

