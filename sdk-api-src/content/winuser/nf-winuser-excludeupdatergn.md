---
UID: NF:winuser.ExcludeUpdateRgn
title: ExcludeUpdateRgn function (winuser.h)
description: The ExcludeUpdateRgn function prevents drawing within invalid areas of a window by excluding an updated region in the window from a clipping region.
old-location: gdi\excludeupdatergn.htm
tech.root: gdi
ms.assetid: 408fda82-30c3-4eb4-be42-3085c71ba99e
ms.date: 12/05/2018
ms.keywords: ExcludeUpdateRgn, ExcludeUpdateRgn function [Windows GDI], _win32_ExcludeUpdateRgn, gdi.excludeupdatergn, winuser/ExcludeUpdateRgn
ms.topic: function
f1_keywords:
- winuser/ExcludeUpdateRgn
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getupdaterect">GetUpdateRect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getupdatergn">GetUpdateRgn</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/painting-and-drawing-functions">Painting and Drawing Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/painting-and-drawing">Painting and Drawing Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-updatewindow">UpdateWindow</a>
 

 

