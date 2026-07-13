---
UID: NF:windowsx.Edit_GetLineCount
title: Edit_GetLineCount macro (windowsx.h)
description: Gets the number of lines in the text of an edit control. You can use this macro or send the EM_GETLINECOUNT message explicitly.
helpviewer_keywords: ["Edit_GetLineCount","Edit_GetLineCount macro [Windows Controls]","_win32_Edit_GetLineCount","_win32_Edit_GetLineCount_cpp","controls.Edit_GetLineCount","controls._win32_Edit_GetLineCount","windowsx/Edit_GetLineCount"]
old-location: controls\Edit_GetLineCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_getlinecount.htm
ms.date: 10/21/2024
ms.keywords: Edit_GetLineCount, Edit_GetLineCount macro [Windows Controls], _win32_Edit_GetLineCount, _win32_Edit_GetLineCount_cpp, controls.Edit_GetLineCount, controls._win32_Edit_GetLineCount, windowsx/Edit_GetLineCount
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
 - Edit_GetLineCount
 - windowsx/Edit_GetLineCount
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
 - Edit_GetLineCount
---

# Edit_GetLineCount macro

## -syntax

```cpp
int Edit_GetLineCount(
   HWND hwndCtl
);
```

## -returns

Type: **int**

The return value is an integer specifying the total number of text lines in the multiline edit control or rich edit control. If the control has no text, the return value is 1. The return value will never be less than 1.


## -description

Gets the number of lines in the text of an edit control. You can use this macro or send the <a href="/windows/desktop/Controls/em-getlinecount">EM_GETLINECOUNT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

## -remarks

For more information, see <a href="/windows/desktop/Controls/em-getlinecount">EM_GETLINECOUNT</a>
