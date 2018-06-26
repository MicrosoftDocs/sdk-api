---
UID: NF:winuser.IsChild
title: IsChild function
author: windows-sdk-content
description: Determines whether a window is a child window or descendant window of a specified parent window.
old-location: winmsg\ischild.htm
old-project: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\windows\windowreference\windowfunctions\ischild.htm
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: IsChild, IsChild function [Windows and Messages], _win32_IsChild, _win32_ischild_cpp, winmsg.ischild, winui._win32_ischild, winuser/IsChild
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
 - User32.dll
 - API-MS-Win-NTUser-IE-Window-l1-1-0.dll
 - ie_shims.dll
 - API-MS-Win-RTCore-NTUser-Window-l1-1-0.dll
 - minuser.dll
 - Ext-MS-Win-NTUser-Window-l1-1-0.dll
 - Ext-MS-Win-NTUser-Window-l1-1-1.dll
 - Ext-MS-Win-NTUser-Window-l1-1-2.dll
 - Ext-MS-Win-RTCore-NTUser-Window-Ext-l1-1-0.dll
 - ext-ms-win-ntuser-window-l1-1-3.dll
 - Ext-MS-Win-NTUser-Window-L1-1-4.dll
api_name:
 - IsChild
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IsChild function


## -description


Determines whether a window is a child window or descendant window of a specified parent window. A child window is the direct descendant of a specified parent window if that parent window is in the chain of parent windows; the chain of parent windows leads from the original overlapped or pop-up window to the child window. 


## -parameters




### -param hWndParent [in]

Type: <b>HWND</b>

A handle to the parent window. 


### -param hWnd [in]

Type: <b>HWND</b>

A handle to the window to be tested. 


## -returns



Type: <strong>Type: <b>BOOL</b>
</strong>

If the window is a child or descendant window of the specified parent window, the return value is nonzero.

If the window is not a child or descendant window of the specified parent window, the return value is zero.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/bd70f81a-e576-4937-bd9b-eac2939b2817">IsWindow</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/a13f1cfc-dedc-4190-826f-b29b731e76df">SetParent</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt637455">Windows</a>
 

 

