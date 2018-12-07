---
UID: NF:winuser.GetCursorInfo
title: GetCursorInfo function
author: windows-sdk-content
description: Retrieves information about the global cursor.
old-location: menurc\getcursorinfo.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\getcursorinfo.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCursorInfo, GetCursorInfo function [Menus and Other Resources], _win32_GetCursorInfo, _win32_getcursorinfo_cpp, menurc.getcursorinfo, winui._win32_getcursorinfo, winuser/GetCursorInfo
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
 - Ext-MS-Win-NTUser-GUI-l1-1-0.dll
 - Ext-MS-Win-NTUser-GUI-l1-1-1.dll
 - Ext-MS-Win-NTUser-GUI-l1-2-0.dll
 - api-ms-win-ntuser-ie-gui-l1-1-0.dll
 - ie_stubs.dll
 - ext-ms-win-ntuser-gui-l1-2-1.dll
 - Ext-MS-Win-RTCore-NTUser-Cursor-L1-1-0.dll
 - MinUser.dll
api_name:
 - GetCursorInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetCursorInfo function


## -description


Retrieves information about the global cursor.


## -parameters




### -param pci [in, out]

Type: <b>PCURSORINFO</b>

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms648381(v=VS.85).aspx">CURSORINFO</a> structure that receives the information. Note that you must set the <b>cbSize</b> member to <code>sizeof(CURSORINFO)</code> before calling this function. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648381(v=VS.85).aspx">CURSORINFO</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646970(v=VS.85).aspx">Cursors</a>



<a href="https://msdn.microsoft.com/en-us/library/ms633506(v=VS.85).aspx">GetGUIThreadInfo</a>



<b>Reference</b>
 

 

