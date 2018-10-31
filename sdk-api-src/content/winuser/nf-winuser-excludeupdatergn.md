---
UID: NF:winuser.ExcludeUpdateRgn
title: ExcludeUpdateRgn function
author: windows-sdk-content
description: The ExcludeUpdateRgn function prevents drawing within invalid areas of a window by excluding an updated region in the window from a clipping region.
old-location: gdi\excludeupdatergn.htm
tech.root: gdi
ms.assetid: 408fda82-30c3-4eb4-be42-3085c71ba99e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ExcludeUpdateRgn, ExcludeUpdateRgn function [Windows GDI], _win32_ExcludeUpdateRgn, gdi.excludeupdatergn, winuser/ExcludeUpdateRgn
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
api_name:
 - ExcludeUpdateRgn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ExcludeUpdateRgn function


## -description


The <b>ExcludeUpdateRgn</b> function prevents drawing within invalid areas of a window by excluding an updated region in the window from a clipping region.


## -parameters




### -param hDC [in]

Handle to the device context associated with the clipping region.


### -param hWnd [in]

Handle to the window to update.


## -returns



The return value specifies the complexity of the excluded region; it can be any one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>COMPLEXREGION</td>
<td>Region consists of more than one rectangle.</td>
</tr>
<tr>
<td>ERROR</td>
<td>An error occurred.</td>
</tr>
<tr>
<td>NULLREGION</td>
<td>Region is empty.</td>
</tr>
<tr>
<td>SIMPLEREGION</td>
<td>Region is a single rectangle.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a>



<a href="https://msdn.microsoft.com/e54483a1-8738-4b22-a24e-c0b31f6ca9d6">GetUpdateRect</a>



<a href="https://msdn.microsoft.com/d80c4b44-3f50-46f9-bf5a-fff7868d91ba">GetUpdateRgn</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/51a50f1f-7b4d-4acd-83a0-1877f5181766">UpdateWindow</a>
 

 

