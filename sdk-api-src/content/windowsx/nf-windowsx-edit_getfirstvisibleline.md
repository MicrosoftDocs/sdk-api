---
UID: NF:windowsx.Edit_GetFirstVisibleLine
title: Edit_GetFirstVisibleLine macro (windowsx.h)
description: Gets the index of the uppermost visible line in a multiline edit or rich edit control. You can use this macro or send the EM_GETFIRSTVISIBLELINE message explicitly.
helpviewer_keywords: ["Edit_GetFirstVisibleLine","Edit_GetFirstVisibleLine macro [Windows Controls]","_win32_Edit_GetFirstVisibleLine","_win32_Edit_GetFirstVisibleLine_cpp","controls.Edit_GetFirstVisibleLine","controls._win32_Edit_GetFirstVisibleLine","windowsx/Edit_GetFirstVisibleLine"]
old-location: controls\Edit_GetFirstVisibleLine.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_getfirstvisibleline.htm
ms.date: 10/21/2024
ms.keywords: Edit_GetFirstVisibleLine, Edit_GetFirstVisibleLine macro [Windows Controls], _win32_Edit_GetFirstVisibleLine, _win32_Edit_GetFirstVisibleLine_cpp, controls.Edit_GetFirstVisibleLine, controls._win32_Edit_GetFirstVisibleLine, windowsx/Edit_GetFirstVisibleLine
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
 - Edit_GetFirstVisibleLine
 - windowsx/Edit_GetFirstVisibleLine
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
 - Edit_GetFirstVisibleLine
---

# Edit_GetFirstVisibleLine macro

## -syntax

```cpp
int Edit_GetFirstVisibleLine(
   HWND hwndCtl
);
```

## -returns

Type: **int**

The zero-based index of the uppermost visible line in a multiline edit control.

<b>Edit controls:</b> For single-line edit controls, the return value is the zero-based index of the first visible character.

<b>Rich edit controls:</b> For single-line rich edit controls, the return value is zero.

## -description

Gets the index of the uppermost visible line in a multiline edit or rich edit control. You can use this macro or send the <a href="/windows/desktop/Controls/em-getfirstvisibleline">EM_GETFIRSTVISIBLELINE</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

## -remarks

For more information, see <a href="/windows/desktop/Controls/em-getfirstvisibleline">EM_GETFIRSTVISIBLELINE</a>.
