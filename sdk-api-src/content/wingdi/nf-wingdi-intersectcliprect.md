---
UID: NF:wingdi.IntersectClipRect
title: IntersectClipRect function
author: windows-sdk-content
description: The IntersectClipRect function creates a new clipping region from the intersection of the current clipping region and the specified rectangle.
old-location: gdi\intersectcliprect.htm
tech.root: gdi
ms.assetid: 9b3f9bfb-337b-45f0-b9ec-399e5f563638
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IntersectClipRect, IntersectClipRect function [Windows GDI], _win32_IntersectClipRect, gdi.intersectcliprect, wingdi/IntersectClipRect
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
 - Ext-MS-Win-GDI-rgn-l1-1-0.dll
 - Ext-MS-Win-RTCore-GDI-rgn-l1-1-0.dll
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
 - API-MS-Win-GDI-Internal-Uap-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - IntersectClipRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IntersectClipRect function


## -description


The <b>IntersectClipRect</b> function creates a new clipping region from the intersection of the current clipping region and the specified rectangle.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param left [in]

The x-coordinate, in logical units, of the upper-left corner of the rectangle.


### -param top [in]

The y-coordinate, in logical units, of the upper-left corner of the rectangle.


### -param right [in]

The x-coordinate, in logical units, of the lower-right corner of the rectangle.


### -param bottom [in]

The y-coordinate, in logical units, of the lower-right corner of the rectangle.


## -returns



The return value specifies the new clipping region's type and can be one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NULLREGION</b></dt>
</dl>
</td>
<td width="60%">
Region is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SIMPLEREGION</b></dt>
</dl>
</td>
<td width="60%">
Region is a single rectangle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMPLEXREGION</b></dt>
</dl>
</td>
<td width="60%">
Region is more than one rectangle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred. (The current clipping region is unaffected.)

</td>
</tr>
</table>
 




## -remarks



The lower and right-most edges of the given rectangle are excluded from the clipping region.

If a clipping region does not already exist then the system may apply a default clipping region to the specified HDC. A clipping region is then created from the intersection of that default clipping region and the rectangle specified in the function parameters.




## -see-also




<a href="https://msdn.microsoft.com/de9e5786-63d8-47be-8522-e96d7c0f8634">Clipping Functions</a>



<a href="https://msdn.microsoft.com/9e966369-9988-4bfa-af37-b1bbb3488880">Clipping Overview</a>



<a href="https://msdn.microsoft.com/5b29c44a-3959-498e-8327-c42ef16a8609">ExcludeClipRect</a>
 

 

