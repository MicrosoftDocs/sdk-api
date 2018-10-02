---
UID: NF:winuser.GetUpdateRgn
title: GetUpdateRgn function
author: windows-sdk-content
description: The GetUpdateRgn function retrieves the update region of a window by copying it into the specified region. The coordinates of the update region are relative to the upper-left corner of the window (that is, they are client coordinates).
old-location: gdi\getupdatergn.htm
tech.root: gdi
ms.assetid: d80c4b44-3f50-46f9-bf5a-fff7868d91ba
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetUpdateRgn, GetUpdateRgn function [Windows GDI], _win32_GetUpdateRgn, gdi.getupdatergn, winuser/GetUpdateRgn
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
 - Ext-MS-Win-NTUser-Draw-l1-1-0.dll
 - Ext-MS-Win-NTUser-Draw-l1-1-1.dll
 - ext-ms-win-ntuser-draw-l1-1-2.dll
api_name:
 - GetUpdateRgn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetUpdateRgn function


## -description


The <b>GetUpdateRgn</b> function retrieves the update region of a window by copying it into the specified region. The coordinates of the update region are relative to the upper-left corner of the window (that is, they are client coordinates).


## -parameters




### -param hWnd [in]

Handle to the window with an update region that is to be retrieved.


### -param hRgn [in]

Handle to the region to receive the update region.


### -param bErase [in]

Specifies whether the window background should be erased and whether nonclient areas of child windows should be drawn. If this parameter is <b>FALSE</b>, no drawing is done.


## -returns



The return value indicates the complexity of the resulting region; it can be one of the following values.

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
 




## -remarks



The <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a> function automatically validates the update region, so any call to <b>GetUpdateRgn</b> made immediately after the call to <b>BeginPaint</b> retrieves an empty update region.




## -see-also




<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>
 

 

