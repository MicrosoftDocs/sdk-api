---
UID: NF:windowsx.Edit_SetRectNoPaint
title: Edit_SetRectNoPaint macro (windowsx.h)
description: Sets the formatting rectangle of a multiline edit control. This macro is equivalent to Edit_SetRect, except that it does not redraw the edit control window. You can use this macro or send the EM_SETRECTNP message explicitly.
helpviewer_keywords: ["Edit_SetRectNoPaint","Edit_SetRectNoPaint macro [Windows Controls]","_win32_Edit_SetRectNoPaint","_win32_Edit_SetRectNoPaint_cpp","controls.Edit_SetRectNoPaint","controls._win32_Edit_SetRectNoPaint","windowsx/Edit_SetRectNoPaint"]
old-location: controls\Edit_SetRectNoPaint.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_setrectnopaint.htm
ms.date: 10/21/2024
ms.keywords: Edit_SetRectNoPaint, Edit_SetRectNoPaint macro [Windows Controls], _win32_Edit_SetRectNoPaint, _win32_Edit_SetRectNoPaint_cpp, controls.Edit_SetRectNoPaint, controls._win32_Edit_SetRectNoPaint, windowsx/Edit_SetRectNoPaint
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
 - Edit_SetRectNoPaint
 - windowsx/Edit_SetRectNoPaint
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
 - Edit_SetRectNoPaint
---

# Edit_SetRectNoPaint macro

## -syntax

```cpp
void Edit_SetRectNoPaint(
   HWND hwndCtl,
   RECT *lprc
);
```


## -description

Sets the formatting rectangle of a multiline edit control. This macro is equivalent to <a href="/windows/desktop/api/windowsx/nf-windowsx-edit_setrect">Edit_SetRect</a>, except that it does not redraw the edit control window. You can use this macro or send the <a href="/windows/desktop/Controls/em-setrectnp">EM_SETRECTNP</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param lprc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the dimensions of the rectangle. If this parameter is <b>NULL</b>, the formatting rectangle is set to its default values.

## -remarks

<b>Rich Edit 3.0 and later.</b> This macro does not have full functionality, because it does not set the WPARAM of the message.

For more information, see <a href="/windows/desktop/Controls/em-setrectnp">EM_SETRECTNP</a>.
