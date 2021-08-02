---
UID: NF:windowsx.Edit_FmtLines
title: Edit_FmtLines macro (windowsx.h)
description: Sets a flag that determines whether text retrieved from a multiline edit control includes soft line-break characters.
helpviewer_keywords: ["Edit_FmtLines","Edit_FmtLines macro [Windows Controls]","_win32_Edit_FormatLines","_win32_Edit_FormatLines_cpp","controls.Edit_FormatLines","controls._win32_Edit_FormatLines","windowsx/Edit_FmtLines"]
old-location: controls\Edit_FormatLines.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_formatlines.htm
ms.date: 12/05/2018
ms.keywords: Edit_FmtLines, Edit_FmtLines macro [Windows Controls], _win32_Edit_FormatLines, _win32_Edit_FormatLines_cpp, controls.Edit_FormatLines, controls._win32_Edit_FormatLines, windowsx/Edit_FmtLines
req.header: windowsx.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Edit_FmtLines
 - windowsx/Edit_FmtLines
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - Edit_FmtLines
---

# Edit_FmtLines macro


## -description

Sets a flag that determines whether text retrieved from a multiline edit control includes soft line-break characters. A soft line break consists of two carriage returns and a line feed and is inserted at the end of a line that is broken because of word wrapping. You can use this macro or send the <a href="/windows/desktop/Controls/em-fmtlines">EM_FMTLINES</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param fAddEOL

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> to insert line breaks; otherwise <b>FALSE</b>.

## -remarks

For more information, see <a href="/windows/desktop/Controls/em-fmtlines">EM_FMTLINES</a>.