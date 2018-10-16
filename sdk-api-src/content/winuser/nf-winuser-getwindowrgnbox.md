---
UID: NF:winuser.GetWindowRgnBox
title: GetWindowRgnBox function
author: windows-sdk-content
description: The GetWindowRgnBox function retrieves the dimensions of the tightest bounding rectangle for the window region of a window.
old-location: gdi\getwindowrgnbox.htm
tech.root: gdi
ms.assetid: 20e23474-a1c5-4afe-976e-a7e5790fb91b
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetWindowRgnBox, GetWindowRgnBox function [Windows GDI], _win32_GetWindowRgnBox, gdi.getwindowrgnbox, winuser/GetWindowRgnBox
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
 - GetWindowRgnBox
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetWindowRgnBox function


## -description


The <b>GetWindowRgnBox</b> function retrieves the dimensions of the tightest bounding rectangle for the window region of a window.


## -parameters




### -param hWnd [in]

Handle to the window.


### -param lprc [out]

Pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that receives the rectangle dimensions, in device units relative to the upper-left corner of the window.


## -returns



The return value specifies the type of the region that the function obtains. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>COMPLEXREGION</td>
<td>The region is more than one rectangle.</td>
</tr>
<tr>
<td>ERROR</td>
<td>The specified window does not have a region, or an error occurred while attempting to return the region.</td>
</tr>
<tr>
<td>NULLREGION</td>
<td>The region is empty.</td>
</tr>
<tr>
<td>SIMPLEREGION</td>
<td>The region is a single rectangle.</td>
</tr>
</table>
 




## -remarks



The window region determines the area within the window where the system permits drawing. The system does not display any portion of a window that lies outside of the window region. The coordinates of a window's window region are relative to the upper-left corner of the window, not the client area of the window.

To set the window region of a window, call the <a href="https://msdn.microsoft.com/06209d0c-14f9-45ec-ae2c-9cc596b5bbaa">SetWindowRgn</a> function.




## -see-also




<a href="https://msdn.microsoft.com/b4ee68ab-b99e-48b6-90ce-6d6c0ae144e2">GetClipBox</a>



<a href="https://msdn.microsoft.com/c8a8fa46-354b-489e-b016-fd2e728958ce">GetWindowRgn</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>



<a href="https://msdn.microsoft.com/06209d0c-14f9-45ec-ae2c-9cc596b5bbaa">SetWindowRgn</a>
 

 

