---
UID: NS:shlobj_core.NT_CONSOLE_PROPS
title: NT_CONSOLE_PROPS (shlobj_core.h)
description: Holds an extra data block used by IShellLinkDataList. It holds console properties.
helpviewer_keywords: ["*LPNT_CONSOLE_PROPS","LPNT_CONSOLE_PROPS","LPNT_CONSOLE_PROPS structure pointer [Windows Shell]","NT_CONSOLE_PROPS","NT_CONSOLE_PROPS structure [Windows Shell]","_win32_NT_CONSOLE_PROPS_str","shell.NT_CONSOLE_PROPS_str","shlobj_core/LPNT_CONSOLE_PROPS","shlobj_core/NT_CONSOLE_PROPS"]
old-location: shell\NT_CONSOLE_PROPS_str.htm
tech.root: shell
ms.assetid: 02542cd4-be8f-45c0-ad0f-e1e39a45f5de
ms.date: 12/05/2018
ms.keywords: '*LPNT_CONSOLE_PROPS, LPNT_CONSOLE_PROPS, LPNT_CONSOLE_PROPS structure pointer [Windows Shell], NT_CONSOLE_PROPS, NT_CONSOLE_PROPS structure [Windows Shell], _win32_NT_CONSOLE_PROPS_str, shell.NT_CONSOLE_PROPS_str, shlobj_core/LPNT_CONSOLE_PROPS, shlobj_core/NT_CONSOLE_PROPS'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NT_CONSOLE_PROPS, *LPNT_CONSOLE_PROPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPNT_CONSOLE_PROPS
 - shlobj_core/LPNT_CONSOLE_PROPS
 - NT_CONSOLE_PROPS
 - shlobj_core/NT_CONSOLE_PROPS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shlobj_core.h
api_name:
 - NT_CONSOLE_PROPS
---

# NT_CONSOLE_PROPS structure


## -description

Holds an extra data block used by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinkdatalist">IShellLinkDataList</a>. It holds console properties.

## -struct-fields

### -field dbh

Type: <b><a href="/windows/win32/api/shlobj_core/ns-shlobj_core-datablock_header">DATABLOCK_HEADER</a></b>

The <a href="/windows/win32/api/shlobj_core/ns-shlobj_core-datablock_header">DATABLOCK_HEADER</a> structure with the <b>NT_CONSOLE_PROPS</b> structure's size and signature. The signature for an <b>NT_CONSOLE_PROPS</b> structure is NT_CONSOLE_PROPS_SIG.

### -field DUMMYSTRUCTNAME

### -field wFillAttribute

Type: <b>WORD</b>

Fill attribute for the console.

### -field wPopupFillAttribute

Type: <b>WORD</b>

Fill attribute for console pop-ups.

### -field dwScreenBufferSize

Type: <b><a href="/windows/console/coord-str">COORD</a></b>

A <a href="/windows/console/coord-str">COORD</a> structure with the console's screen buffer size.

### -field dwWindowSize

Type: <b><a href="/windows/console/coord-str">COORD</a></b>

A <a href="/windows/console/coord-str">COORD</a> structure with the console's window size.

### -field dwWindowOrigin

Type: <b><a href="/windows/console/coord-str">COORD</a></b>

A <a href="/windows/console/coord-str">COORD</a> structure with the console's window origin.

### -field nFont

Type: <b>DWORD</b>

The font.

### -field nInputBufferSize

Type: <b>DWORD</b>

The input buffer size.

### -field dwFontSize

Type: <b><a href="/windows/console/coord-str">COORD</a></b>

A <a href="/windows/console/coord-str">COORD</a> structure with the font size.

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

Type: <b><a href="/windows/desktop/gdi/colorref">COLORREF</a>[16]</b>

An array of <a href="/windows/desktop/gdi/colorref">COLORREF</a> values with the console's color settings.

