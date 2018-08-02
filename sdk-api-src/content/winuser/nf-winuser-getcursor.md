---
UID: NF:winuser.GetCursor
title: GetCursor function
author: windows-sdk-content
description: Retrieves a handle to the current cursor.
old-location: menurc\getcursor.htm
old-project: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\getcursor.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetCursor, GetCursor function [Menus and Other Resources], _win32_GetCursor, _win32_getcursor_cpp, menurc.getcursor, winui._win32_getcursor, winuser/GetCursor
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-0.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - api-ms-win-ntuser-ie-gui-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-RTCore-NTUser-Cursor-L1-1-0.dll
 - MinUser.dll
api_name:
 - GetCursor
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# GetCursor function


## -description


Retrieves a handle to the current cursor.

To get information on the global cursor, even if it is not owned by the current thread, use <a href="https://msdn.microsoft.com/en-us/library/ms648389(v=VS.85).aspx">GetCursorInfo</a>.


## -parameters






## -returns



Type: <b>HCURSOR</b>

The return value is the handle to the current cursor. If there is no cursor, the return value is <b>NULL</b>. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646970(v=VS.85).aspx">Cursors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648389(v=VS.85).aspx">GetCursorInfo</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648393(v=VS.85).aspx">SetCursor</a>
 

 

