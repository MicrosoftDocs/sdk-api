---
UID: NF:windowsx.Edit_SetHandle
title: Edit_SetHandle macro (windowsx.h)
description: Sets the handle of the memory that will be used by a multiline edit control. You can use this macro or send the EM_SETHANDLE message explicitly.
helpviewer_keywords: ["Edit_SetHandle","Edit_SetHandle macro [Windows Controls]","_win32_Edit_SetHandle","_win32_Edit_SetHandle_cpp","controls.Edit_SetHandle","controls._win32_Edit_SetHandle","windowsx/Edit_SetHandle"]
old-location: controls\Edit_SetHandle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_sethandle.htm
ms.date: 10/21/2024
ms.keywords: Edit_SetHandle, Edit_SetHandle macro [Windows Controls], _win32_Edit_SetHandle, _win32_Edit_SetHandle_cpp, controls.Edit_SetHandle, controls._win32_Edit_SetHandle, windowsx/Edit_SetHandle
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
 - Edit_SetHandle
 - windowsx/Edit_SetHandle
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
 - Edit_SetHandle
---

# Edit_SetHandle macro

## -syntax

```cpp
void Edit_SetHandle(
   HWND   hwndCtl,
   HLOCAL h
);
```


## -description

Sets the handle of the memory that will be used by a multiline edit control. You can use this macro or send the <a href="/windows/desktop/Controls/em-sethandle">EM_SETHANDLE</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param h

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HLOCAL</a></b>

A handle to the memory buffer the edit control uses to store the currently displayed text instead of allocating its own memory. If necessary, the control reallocates this memory.

## -remarks

For more information, see <a href="/windows/desktop/Controls/em-sethandle">EM_SETHANDLE</a>.
