---
UID: NF:windowsx.Edit_GetHandle
title: Edit_GetHandle macro (windowsx.h)
description: Gets a handle to the memory currently allocated for the text of a multiline edit control. You can use this macro or send the EM_GETHANDLE message explicitly.
helpviewer_keywords: ["Edit_GetHandle","Edit_GetHandle macro [Windows Controls]","_win32_Edit_GetHandle","_win32_Edit_GetHandle_cpp","controls.Edit_GetHandle","controls._win32_Edit_GetHandle","windowsx/Edit_GetHandle"]
old-location: controls\Edit_GetHandle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_gethandle.htm
ms.date: 10/21/2024
ms.keywords: Edit_GetHandle, Edit_GetHandle macro [Windows Controls], _win32_Edit_GetHandle, _win32_Edit_GetHandle_cpp, controls.Edit_GetHandle, controls._win32_Edit_GetHandle, windowsx/Edit_GetHandle
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
 - Edit_GetHandle
 - windowsx/Edit_GetHandle
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
 - Edit_GetHandle
---

# Edit_GetHandle macro

## -syntax

```cpp
HLOCAL Edit_GetHandle(
   HWND hwndCtl
);
```

## -returns

Type: **[HLOCAL](/windows/desktop/winprog/windows-data-types)**

A memory handle identifying the buffer that holds the content of the edit control. If an error occurs, such as sending the message to a single-line edit control, the return value is zero.


## -description

Gets a handle to the memory currently allocated for the text of a multiline edit control. You can use this macro or send the <a href="/windows/desktop/Controls/em-gethandle">EM_GETHANDLE</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

## -remarks

For more information, see <a href="/windows/desktop/Controls/em-gethandle">EM_GETHANDLE</a>.
