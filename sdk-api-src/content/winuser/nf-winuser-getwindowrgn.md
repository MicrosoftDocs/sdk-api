---
UID: NF:winuser.GetWindowRgn
title: GetWindowRgn function
author: windows-driver-content
description: The GetWindowRgn function obtains a copy of the window region of a window.
old-location: gdi\getwindowrgn.htm
old-project: gdi
ms.assetid: c8a8fa46-354b-489e-b016-fd2e728958ce
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetWindowRgn, GetWindowRgn function [Windows GDI], _win32_GetWindowRgn, gdi.getwindowrgn, winuser/GetWindowRgn
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
-	Ext-MS-Win-NTUser-Draw-L1-1-2.dll
api_name:
-	GetWindowRgn
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetWindowRgn function


## -description


The <b>GetWindowRgn</b> function obtains a copy of the window region of a window. The window region of a window is set by calling the <a href="https://msdn.microsoft.com/06209d0c-14f9-45ec-ae2c-9cc596b5bbaa">SetWindowRgn</a> function. The window region determines the area within the window where the system permits drawing. The system does not display any portion of a window that lies outside of the window region


## -parameters




### -param hWnd [in]

Handle to the window whose window region is to be obtained.


### -param hRgn [in]

Handle to the region which will be modified to represent the window region.


## -returns



The return value specifies the type of the region that the function obtains. It can be one of the following values.

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
The region is empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SIMPLEREGION</b></dt>
</dl>
</td>
<td width="60%">
The region is a single rectangle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>COMPLEXREGION</b></dt>
</dl>
</td>
<td width="60%">
The region is more than one rectangle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR</b></dt>
</dl>
</td>
<td width="60%">
The specified window does not have a region, or an error occurred while attempting to return the region.

</td>
</tr>
</table>
 




## -remarks



The coordinates of a window's window region are relative to the upper-left corner of the window, not the client area of the window.

To set the window region of a window, call the <a href="https://msdn.microsoft.com/06209d0c-14f9-45ec-ae2c-9cc596b5bbaa">SetWindowRgn</a> function.


#### Examples

The following code shows how you pass in the handle of an existing region.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRGN hrgn = CreateRectRgn(0,0,0,0);
int regionType = GetWindowRgn(hwnd, hrgn);
if (regionType != ERROR) 
{ 
/* hrgn contains window region */ 
}
DeleteObject(hrgn); /* finished with region */
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="https://msdn.microsoft.com/06209d0c-14f9-45ec-ae2c-9cc596b5bbaa">SetWindowRgn</a>
 

 

