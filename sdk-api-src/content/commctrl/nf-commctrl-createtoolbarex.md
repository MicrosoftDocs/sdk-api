---
UID: NF:commctrl.CreateToolbarEx
title: CreateToolbarEx function (commctrl.h)
description: Creates a toolbar window and adds the specified buttons to the toolbar.
helpviewer_keywords: ["CreateToolbarEx","CreateToolbarEx function [Windows Controls]","_win32_CreateToolbarEx","_win32_CreateToolbarEx_cpp","commctrl/CreateToolbarEx","controls.CreateToolbarEx","controls._win32_CreateToolbarEx"]
old-location: controls\CreateToolbarEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\toolbar\functions\createtoolbarex.htm
ms.date: 12/05/2018
ms.keywords: CreateToolbarEx, CreateToolbarEx function [Windows Controls], _win32_CreateToolbarEx, _win32_CreateToolbarEx_cpp, commctrl/CreateToolbarEx, controls.CreateToolbarEx, controls._win32_CreateToolbarEx
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateToolbarEx
 - commctrl/CreateToolbarEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - CreateToolbarEx
req.apiset: ext-ms-win-shell-comctl32-window-l1-1-0 (introduced in Windows 10, version 10.0.14393)
---

# CreateToolbarEx function


## -description

Creates a toolbar window and adds the specified buttons to the toolbar. 
			
<div class="alert"><b>Note</b>   This function is deprecated, because it does not support all features of toolbars. Use <a href="/windows/desktop/api/winuser/nf-winuser-createwindowexa">CreateWindowEx</a> instead. For examples, see <a href="/windows/desktop/Controls/using-toolbar-controls">Using Toolbar Controls</a>.</div><div> </div>

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the parent window for the toolbar.

### -param ws

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Window styles for the toolbar. The <a href="/windows/desktop/winmsg/window-styles">WS_CHILD</a> style is included by default. This parameter can also include a combination of styles as discussed in <a href="/windows/desktop/Controls/toolbar-control-and-button-styles">Toolbar Control and Button Styles</a>.

### -param wID

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Control identifier for the toolbar.

### -param nBitmaps

Type: <b>int</b>

Number of button images contained in the bitmap specified by 
					<i>hBMInst</i> and 
					<i>wBMID</i>.

### -param hBMInst

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

Module instance with the executable file that contains the bitmap resource.

### -param wBMID

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT_PTR</a></b>

Resource identifier for the bitmap resource. If 
					<i>hBMInst</i> is <b>NULL</b>, this parameter must be a valid bitmap handle.

### -param lpButtons

Type: <b>LPCTBBUTTON</b>

Pointer to an array of <a href="/windows/desktop/api/commctrl/ns-commctrl-tbbutton">TBBUTTON</a> structures that contain information about the buttons to add to the toolbar.

### -param iNumButtons

Type: <b>int</b>

Number of buttons to add to the toolbar.

### -param dxButton

Type: <b>int</b>

Width, in pixels, of the buttons to add to the toolbar.

### -param dyButton

Type: <b>int</b>

Height, in pixels, of the buttons to add to the toolbar.

### -param dxBitmap

Type: <b>int</b>

Width, in pixels, of the button images to add to the buttons in the toolbar.

### -param dyBitmap

Type: <b>int</b>

Height, in pixels, of the button images to add to the buttons in the toolbar.

### -param uStructSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Size of a <a href="/windows/desktop/api/commctrl/ns-commctrl-tbbutton">TBBUTTON</a> structure.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Returns the window handle to the toolbar if successful, or <b>NULL</b> otherwise. To retrieve extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Windows 95: The system can support a maximum of 16,364 window handles.
