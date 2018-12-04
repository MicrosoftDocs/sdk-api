---
UID: NF:winuser.GetCursor
title: GetCursor function
author: windows-sdk-content
description: Retrieves a handle to the current cursor.
old-location: menurc\getcursor.htm
tech.root: menurc
ms.assetid: VS|winui|~\winui\windowsuserinterface\resources\cursors\cursorreference\cursorfunctions\getcursor.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetCursor, GetCursor function [Menus and Other Resources], _win32_GetCursor, _win32_getcursor_cpp, menurc.getcursor, winui._win32_getcursor, winuser/GetCursor
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
 - GetCursor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetCursor function


## -description


Retrieves a handle to the current cursor.

To get information on the global cursor, even if it is not owned by the current thread, use <a href="https://msdn.microsoft.com/4dea42e7-f78f-4e34-9e1d-e76123a209fc">GetCursorInfo</a>.


## -parameters






## -returns



Type: <b>HCURSOR</b>

The return value is the handle to the current cursor. If there is no cursor, the return value is <b>NULL</b>. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d24e21f2-224d-4f32-aa0b-70844e3628ad">Cursors</a>



<a href="https://msdn.microsoft.com/4dea42e7-f78f-4e34-9e1d-e76123a209fc">GetCursorInfo</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/69bb9f90-5366-4141-97b6-57e41b774614">SetCursor</a>
 

 

