---
UID: NF:winuser.CreateMDIWindowW
title: CreateMDIWindowW function
author: windows-sdk-content
description: Creates a multiple-document interface (MDI) child window.
old-location: winmsg\createmdiwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface\multipledocumentinterfacereference\multipledocumentinterfacefunctions\createmdiwindow.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateMDIWindow, CreateMDIWindow function [Windows and Messages], CreateMDIWindowA, CreateMDIWindowW, WS_HSCROLL, WS_MAXIMIZE, WS_MINIMIZE, WS_VSCROLL, _win32_CreateMDIWindow, _win32_createmdiwindow_cpp, winmsg.createmdiwindow, winui._win32_createmdiwindow, winuser/CreateMDIWindow, winuser/CreateMDIWindowA, winuser/CreateMDIWindowW
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
req.unicode-ansi: CreateMDIWindowW (Unicode) and CreateMDIWindowA (ANSI)
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
api_name:
 - CreateMDIWindow
 - CreateMDIWindowA
 - CreateMDIWindowW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CreateMDIWindowW
: 
---

# CreateMDIWindowW function


## -description


Creates a multiple-document interface (MDI) child window. 


## -parameters




### -param lpClassName [in]

Type: <b>LPCTSTR</b>

The window class of the MDI child window. The class name must have been registered by a call to the <a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a> function.


### -param lpWindowName [in]

Type: <b>LPCTSTR</b>

The window name. The system displays the name in the title bar of the child window.


### -param dwStyle [in]

Type: <b>DWORD</b>

The style of the MDI child window. If the MDI client window is created with the <b>MDIS_ALLCHILDSTYLES</b> window style, this parameter can be any combination of the window styles listed in the <a href="https://msdn.microsoft.com/bfc146f1-bebd-4e68-a29e-a73ff3e8f35b">Window Styles</a> page. Otherwise, this parameter is limited to one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WS_MINIMIZE"></a><a id="ws_minimize"></a><dl>
<dt><b>WS_MINIMIZE</b></dt>
<dt>0x20000000L</dt>
</dl>
</td>
<td width="60%">
Creates an MDI child window that is initially minimized.

</td>
</tr>
<tr>
<td width="40%"><a id="WS_MAXIMIZE"></a><a id="ws_maximize"></a><dl>
<dt><b>WS_MAXIMIZE</b></dt>
<dt>0x01000000L</dt>
</dl>
</td>
<td width="60%">
Creates an MDI child window that is initially maximized.

</td>
</tr>
<tr>
<td width="40%"><a id="WS_HSCROLL"></a><a id="ws_hscroll"></a><dl>
<dt><b>WS_HSCROLL</b></dt>
<dt>0x00100000L</dt>
</dl>
</td>
<td width="60%">
Creates an MDI child window that has a horizontal scroll bar.

</td>
</tr>
<tr>
<td width="40%"><a id="WS_VSCROLL"></a><a id="ws_vscroll"></a><dl>
<dt><b>WS_VSCROLL</b></dt>
<dt>0x00200000L</dt>
</dl>
</td>
<td width="60%">
Creates an MDI child window that has a vertical scroll bar.

</td>
</tr>
</table>
 


### -param X [in]

Type: <b>int</b>

The initial horizontal position, in client coordinates, of the MDI child window. If this parameter is <b>CW_USEDEFAULT</b> ((int)0x80000000), the MDI child window is assigned the default horizontal position. 


### -param Y [in]

Type: <b>int</b>

The initial vertical position, in client coordinates, of the MDI child window. If this parameter is <b>CW_USEDEFAULT</b>, the MDI child window is assigned the default vertical position. 


### -param nWidth [in]

Type: <b>int</b>

The initial width, in device units, of the MDI child window. If this parameter is <b>CW_USEDEFAULT</b>, the MDI child window is assigned the default width. 


### -param nHeight [in]

Type: <b>int</b>

The initial height, in device units, of the MDI child window. If this parameter is set to <b>CW_USEDEFAULT</b>, the MDI child window is assigned the default height. 


### -param hWndParent [in, optional]

Type: <b>HWND</b>

A handle to the MDI client window that will be the parent of the new MDI child window. 


### -param hInstance [in, optional]

Type: <b>HINSTANCE</b>

A handle to the instance of the application creating the MDI child window. 


### -param lParam [in]

Type: <b>LPARAM</b>

An application-defined value. 


## -returns



Type: <strong>Type: <b>HWND</b>
</strong>

If the function succeeds, the return value is the handle to the created window.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/5424b87c-22ea-414e-840e-214d9f0dc9ad">CreateWindow</a>



<a href="https://msdn.microsoft.com/beb41067-91ed-4f63-af8f-1000ba82a3b1">Multiple Document Interface</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/f48ba5a5-08c7-4d16-bc25-e028ea9a73f4">RegisterClassEx</a>



<a href="https://msdn.microsoft.com/f2313ffd-867f-4870-a667-3e5f5402776f">WM_MDICREATE</a>
 

 

