---
UID: NF:winuser.RealChildWindowFromPoint
title: RealChildWindowFromPoint function
author: windows-sdk-content
description: Retrieves a handle to the child window at the specified point. The search is restricted to immediate child windows; grandchildren and deeper descendant windows are not searched.
old-location: winmsg\realchildwindowfrompoint.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\realchildwindowfrompoint.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: RealChildWindowFromPoint, RealChildWindowFromPoint function [Windows and Messages], _win32_RealChildWindowFromPoint, _win32_realchildwindowfrompoint_cpp, winmsg.realchildwindowfrompoint, winui._win32_realchildwindowfrompoint, winuser/RealChildWindowFromPoint
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
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - minuser.dll
api_name:
 - RealChildWindowFromPoint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RealChildWindowFromPoint function


## -description


Retrieves a handle to the child window at the specified point. The search is restricted to immediate child windows; grandchildren and deeper descendant windows are not searched.


## -parameters




### -param hwndParent [in]

Type: <b>HWND</b>

A handle to the window whose child is to be retrieved. 


### -param ptParentClientCoords [in]

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

A <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that defines the client coordinates of the point to be checked. 


## -returns



Type: <strong>Type: <b>HWND</b>
</strong>

The return value is a handle to the child window that contains the specified point. 




## -remarks



<b>RealChildWindowFromPoint</b> treats <b>HTTRANSPARENT</b> areas of a standard control differently from other areas of the control; it returns the child window behind a transparent part of a control. In contrast, <a href="https://msdn.microsoft.com/30f8ec3d-7b8c-45b6-b659-d417302e16c5">ChildWindowFromPoint</a> treats <b>HTTRANSPARENT</b> areas of a control the same as other areas. For example, if the point is in a transparent area of a groupbox, <b>RealChildWindowFromPoint</b> returns the child window behind a groupbox, whereas <b>ChildWindowFromPoint</b> returns the groupbox. However, both APIs return a static field, even though it, too, returns <b>HTTRANSPARENT</b>.




## -see-also




<a href="https://msdn.microsoft.com/30f8ec3d-7b8c-45b6-b659-d417302e16c5">ChildWindowFromPoint</a>



<b>Conceptual</b>



<b>Other Resources</b>



<a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/e2c778c7-7319-4bf7-a6a7-b526e4f3e98b">Windows</a>
 

 

