---
UID: NS:shlobj_core.NT_CONSOLE_PROPS
title: NT_CONSOLE_PROPS
author: windows-sdk-content
description: Holds an extra data block used by IShellLinkDataList. It holds console properties.
old-location: shell\NT_CONSOLE_PROPS_str.htm
old-project: shell
ms.assetid: 02542cd4-be8f-45c0-ad0f-e1e39a45f5de
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: "*LPNT_CONSOLE_PROPS, LPNT_CONSOLE_PROPS, LPNT_CONSOLE_PROPS structure pointer [Windows Shell], NT_CONSOLE_PROPS, NT_CONSOLE_PROPS structure [Windows Shell], _win32_NT_CONSOLE_PROPS_str, shell.NT_CONSOLE_PROPS_str, shlobj_core/LPNT_CONSOLE_PROPS, shlobj_core/NT_CONSOLE_PROPS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.typenames: NT_CONSOLE_PROPS, *LPNT_CONSOLE_PROPS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - NT_CONSOLE_PROPS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# NT_CONSOLE_PROPS structure


## -description


Holds an extra data block used by <a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>. It holds console properties.


## -struct-fields




### -field dbh

Type: <b><a href="https://msdn.microsoft.com/06de45c2-8cb5-45e3-9639-d4625c24d27b">DATABLOCK_HEADER</a></b>

The <a href="https://msdn.microsoft.com/06de45c2-8cb5-45e3-9639-d4625c24d27b">DATABLOCK_HEADER</a> structure with the <b>NT_CONSOLE_PROPS</b> structure's size and signature. The signature for an <b>NT_CONSOLE_PROPS</b> structure is NT_CONSOLE_PROPS_SIG.


### -field DUMMYSTRUCTNAME

 


### -field wFillAttribute

Type: <b>WORD</b>

Fill attribute for the console.


### -field wPopupFillAttribute

Type: <b>WORD</b>

Fill attribute for console pop-ups.


### -field dwScreenBufferSize

Type: <b><a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a></b>

A <a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure with the console's screen buffer size.


### -field dwWindowSize

Type: <b><a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a></b>

A <a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure with the console's window size.


### -field dwWindowOrigin

Type: <b><a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a></b>

A <a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure with the console's window origin.


### -field nFont

Type: <b>DWORD</b>

The font.


### -field nInputBufferSize

Type: <b>DWORD</b>

The input buffer size.


### -field dwFontSize

Type: <b><a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a></b>

A <a href="https://msdn.microsoft.com/d730c46e-ea17-475e-b956-8ee5f4f5c04e">COORD</a> structure with the font size.


### -field uFontFamily

Type: <b>UINT</b>

The font family.


### -field uFontWeight

Type: <b>UINT</b>

The font weight.


### -field FaceName

Type: <b>WCHAR[LF_FACESIZE]</b>

A character array that contains the font's face name.


### -field uCursorSize

Type: <b>UINT</b>

The cursor size.


### -field bFullScreen

Type: <b>BOOL</b>

A boolean value that is set to <b>TRUE</b> if the console is in full-screen mode, or <b>FALSE</b> otherwise.


### -field bQuickEdit

Type: <b>BOOL</b>

A boolean value that is set to <b>TRUE</b> if the console is in quick-edit mode, or <b>FALSE</b> otherwise.


### -field bInsertMode

Type: <b>BOOL</b>

A boolean value that is set to <b>TRUE</b> if the console is in insert mode, or <b>FALSE</b> otherwise.


### -field bAutoPosition

Type: <b>BOOL</b>

A boolean value that is set to <b>TRUE</b> if the console is in auto-position mode, or <b>FALSE</b> otherwise.


### -field uHistoryBufferSize

Type: <b>UINT</b>

The size of the history buffer.


### -field uNumberOfHistoryBuffers

Type: <b>UINT</b>

The number of history buffers.


### -field bHistoryNoDup

Type: <b>BOOL</b>

A boolean value that is set to <b>TRUE</b> if old duplicate history lists should be discarded, or <b>FALSE</b> otherwise.


### -field ColorTable

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a>[16]</b>

An array of <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> values with the console's color settings.

