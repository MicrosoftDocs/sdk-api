---
UID: NF:winuser.GetCursor
title: GetCursor function (winuser.h)
author: windows-sdk-content
description: Retrieves a handle to the current cursor.
old-location: menurc\getcursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\getcursor.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCursor, GetCursor function [Menus and Other Resources], _win32_GetCursor, _win32_getcursor_cpp, menurc.getcursor, winui._win32_getcursor, winuser/GetCursor
ms.topic: function
f1_keywords: 
 - "winuser/GetCursor"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCursor function


## -description


Retrieves a handle to the current cursor.

To get information on the global cursor, even if it is not owned by the current thread, use <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getcursorinfo">GetCursorInfo</a>.


## -parameters






## -returns



Type: <b>HCURSOR</b>

The return value is the handle to the current cursor. If there is no cursor, the return value is <b>NULL</b>. 




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/menurc/cursors">Cursors</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getcursorinfo">GetCursorInfo</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setcursor">SetCursor</a>
 

 

