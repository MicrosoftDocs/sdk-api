---
UID: NF:winuser.ChildWindowFromPoint
title: ChildWindowFromPoint function
author: windows-sdk-content
description: Determines which, if any, of the child windows belonging to a parent window contains the specified point. The search is restricted to immediate child windows. Grandchildren, and deeper descendant windows are not searched.
old-location: winmsg\childwindowfrompoint.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\childwindowfrompoint.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ChildWindowFromPoint, ChildWindowFromPoint function [Windows and Messages], _win32_ChildWindowFromPoint, _win32_childwindowfrompoint_cpp, winmsg.childwindowfrompoint, winui._win32_childwindowfrompoint, winuser/ChildWindowFromPoint
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
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
api_name:
 - ChildWindowFromPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ChildWindowFromPoint function


## -description


Determines which, if any, 
			of the child windows belonging to a parent window contains the specified point. 
			The search is restricted to immediate child windows. Grandchildren, and deeper 
			descendant windows are not searched.

To skip certain child windows, use the <a href="https://msdn.microsoft.com/ab146c04-5dd3-4807-a256-33822b2531c5">ChildWindowFromPointEx</a> function.


## -parameters




### -param hWndParent [in]

Type: <b>HWND</b>

A handle to the parent window. 


### -param Point [in]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

A structure that defines the client 
				coordinates, relative to <i>hWndParent</i>, 
				of the point to be checked.


## -returns



Type: <strong>Type: <b>HWND</b>
</strong>

The return value is a handle to the child window that contains the point, 
				even if the child window is hidden or disabled. If the point lies outside the 
				parent window, the return value is <b>NULL</b>. If the point is within 
				the parent window but not within any child window, the return value is a handle 
				to the parent window. 




## -remarks



The system maintains an internal list, containing the handles of the child windows 
			associated with a parent window. The order of the handles in the list depends on the Z 
			order of the child windows. If more than one child window contains the specified point, 
			the system returns a handle to the first window in the list that contains the point. 

<b>ChildWindowFromPoint</b> treats an <b>HTTRANSPARENT</b> area of a standard 
			control the same as other parts of the control. In contrast, 
			<a href="https://msdn.microsoft.com/4e386040-112b-4150-a045-c2bb51b536ad">RealChildWindowFromPoint</a> treats an <b>HTTRANSPARENT</b> area differently; 
			it returns the child window behind a transparent area of a control. For example, if the 
			point is in a transparent area of a groupbox, <b>ChildWindowFromPoint</b> 
			returns the groupbox while <b>RealChildWindowFromPoint</b> returns the 
			child window behind the groupbox. However, both APIs return 
			a static field, even though it, too, returns <b>HTTRANSPARENT</b>.


#### Examples

For an example, see "Creating a Combo Box Toolbar" in <a href="_win32_Using_Combo_Boxes">Using Combo Boxes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ab146c04-5dd3-4807-a256-33822b2531c5">ChildWindowFromPointEx</a>



<b>Conceptual</b>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<a href="https://msdn.microsoft.com/4e386040-112b-4150-a045-c2bb51b536ad">RealChildWindowFromPoint</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e4830394-f994-4d29-b843-3a618e331d52">WindowFromPoint</a>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

