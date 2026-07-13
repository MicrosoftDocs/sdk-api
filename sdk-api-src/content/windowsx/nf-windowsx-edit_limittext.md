---
UID: NF:windowsx.Edit_LimitText
title: Edit_LimitText macro (windowsx.h)
description: Limits the length of text that can be entered into an edit control. You can use this macro or send the EM_LIMITTEXT message explicitly.
helpviewer_keywords: ["Edit_LimitText","Edit_LimitText macro [Windows Controls]","_win32_Edit_LimitText","_win32_Edit_LimitText_cpp","controls.Edit_LimitText","controls._win32_Edit_LimitText","windowsx/Edit_LimitText"]
old-location: controls\Edit_LimitText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_limittext.htm
ms.date: 10/21/2024
ms.keywords: Edit_LimitText, Edit_LimitText macro [Windows Controls], _win32_Edit_LimitText, _win32_Edit_LimitText_cpp, controls.Edit_LimitText, controls._win32_Edit_LimitText, windowsx/Edit_LimitText
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
 - Edit_LimitText
 - windowsx/Edit_LimitText
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
 - Edit_LimitText
---

# Edit_LimitText macro

## -syntax

```cpp
void Edit_LimitText(
   HWND hwndCtl,
   int  cchMax
);
```


## -description

Limits the length of text that can be entered into an edit control. You can use this macro or send the <a href="/windows/desktop/Controls/em-limittext">EM_LIMITTEXT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param cchMax

Type: <b>int</b>

The maximum number of characters.

## -remarks

For more information, see <a href="/windows/desktop/Controls/em-limittext">EM_LIMITTEXT</a>.
