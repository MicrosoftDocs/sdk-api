---
UID: NF:commctrl.CreateUpDownControl
title: CreateUpDownControl function (commctrl.h)
description: Creates an up-down control. Note:\_This function is obsolete. It is a 16 bit function and cannot handle 32 bit values for range and position.
helpviewer_keywords: ["CreateUpDownControl","CreateUpDownControl function [Windows Controls]","_win32_CreateUpDownControl","_win32_CreateUpDownControl_cpp","commctrl/CreateUpDownControl","controls.CreateUpDownControl","controls._win32_CreateUpDownControl"]
old-location: controls\CreateUpDownControl.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\updown\functions\createupdowncontrol.htm
ms.date: 12/05/2018
ms.keywords: CreateUpDownControl, CreateUpDownControl function [Windows Controls], _win32_CreateUpDownControl, _win32_CreateUpDownControl_cpp, commctrl/CreateUpDownControl, controls.CreateUpDownControl, controls._win32_CreateUpDownControl
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
 - CreateUpDownControl
 - commctrl/CreateUpDownControl
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
 - CreateUpDownControl
---

# CreateUpDownControl function


## -description

Creates an up-down control. 
			 Note: This function is obsolete. It is a 16 bit function and cannot handle 32 bit values for range and position.

## -parameters

### -param dwStyle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Window styles for the control. This parameter should include the <a href="/windows/desktop/winmsg/window-styles">WS_CHILD</a>, <a href="/windows/desktop/winmsg/window-styles">WS_BORDER</a>, and <a href="/windows/desktop/winmsg/window-styles">WS_VISIBLE</a> styles, and it may include any of the window styles specific to the up-down control.

### -param x

Type: <b>int</b>

Horizontal coordinate, in client coordinates, of the upper-left corner of the control.

### -param y

Type: <b>int</b>

Vertical coordinate, in client coordinates, of the upper-left corner of the control.

### -param cx

Type: <b>int</b>

Width, in pixels, of the up-down control.

### -param cy

Type: <b>int</b>

Height, in pixels, of the up-down control.

### -param hParent

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the parent window of the up-down control.

### -param nID

Type: <b>int</b>

Identifier for the up-down control.

### -param hInst

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HINSTANCE</a></b>

Handle to the module instance of the application creating the up-down control.

### -param hBuddy

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the window associated with the up-down control. If this parameter is <b>NULL</b>, the control has no buddy window.

### -param nUpper

Type: <b>int</b>

Upper limit (range) of the up-down control.

### -param nLower

Type: <b>int</b>

Lower limit (range) of the up-down control.

### -param nPos

Type: <b>int</b>

Position of the control.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

If the function succeeds, the return value is the window handle to the up-down control. If the function fails, the return value is <b>NULL</b>.