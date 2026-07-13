---
UID: NF:winuser.CreateMDIWindowW
title: CreateMDIWindowW function (winuser.h)
description: Creates a multiple-document interface (MDI) child window. (Unicode)
helpviewer_keywords: ["CreateMDIWindow", "CreateMDIWindow function [Windows and Messages]", "CreateMDIWindowW", "WS_HSCROLL", "WS_MAXIMIZE", "WS_MINIMIZE", "WS_VSCROLL", "_win32_CreateMDIWindow", "_win32_createmdiwindow_cpp", "winmsg.createmdiwindow", "winui._win32_createmdiwindow", "winuser/CreateMDIWindow", "winuser/CreateMDIWindowW"]
old-location: winmsg\createmdiwindow.htm
tech.root: winmsg
ms.assetid: VS|winui|~\winui\windowsuserinterface\windowing\multipledocumentinterface\multipledocumentinterfacereference\multipledocumentinterfacefunctions\createmdiwindow.htm
ms.date: 12/05/2018
ms.keywords: CreateMDIWindow, CreateMDIWindow function [Windows and Messages], CreateMDIWindowA, CreateMDIWindowW, WS_HSCROLL, WS_MAXIMIZE, WS_MINIMIZE, WS_VSCROLL, _win32_CreateMDIWindow, _win32_createmdiwindow_cpp, winmsg.createmdiwindow, winui._win32_createmdiwindow, winuser/CreateMDIWindow, winuser/CreateMDIWindowA, winuser/CreateMDIWindowW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateMDIWindowW
 - winuser/CreateMDIWindowW
dev_langs:
 - c++
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
---

# CreateMDIWindowW function


## -description

Creates a multiple-document interface (MDI) child window.

## -parameters

### -param lpClassName [in]

Type: <b>LPCTSTR</b>

The window class of the MDI child window. The class name must have been registered by a call to the <a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a> function.

### -param lpWindowName [in]

Type: <b>LPCTSTR</b>

The window name. The system displays the name in the title bar of the child window.

### -param dwStyle [in]

Type: <b>DWORD</b>

The style of the MDI child window. If the MDI client window is created with the <b>MDIS_ALLCHILDSTYLES</b> window style, this parameter can be any combination of the window styles listed in the <a href="/windows/desktop/winmsg/window-styles">Window Styles</a> page. Otherwise, this parameter is limited to one or more of the following values.

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

Type: <b>HWND</b>

If the function succeeds, the return value is the handle to the created window.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/winuser/nf-winuser-createwindowa">CreateWindow</a>



<a href="/windows/desktop/winmsg/multiple-document-interface">Multiple Document Interface</a>



<b>Reference</b>



<a href="/windows/desktop/api/winuser/nf-winuser-registerclassexa">RegisterClassEx</a>



<a href="/windows/desktop/winmsg/wm-mdicreate">WM_MDICREATE</a>

## -remarks

> [!NOTE]
> The winuser.h header defines CreateMDIWindow as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
