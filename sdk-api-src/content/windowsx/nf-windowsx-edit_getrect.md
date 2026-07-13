---
UID: NF:windowsx.Edit_GetRect
title: Edit_GetRect macro (windowsx.h)
description: Gets the formatting rectangle of an edit control. You can use this macro or send the EM_GETRECT message explicitly.
helpviewer_keywords: ["Edit_GetRect","Edit_GetRect macro [Windows Controls]","_win32_Edit_GetRect","_win32_Edit_GetRect_cpp","controls.Edit_GetRect","controls._win32_Edit_GetRect","windowsx/Edit_GetRect"]
old-location: controls\Edit_GetRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_getrect.htm
ms.date: 10/21/2024
ms.keywords: Edit_GetRect, Edit_GetRect macro [Windows Controls], _win32_Edit_GetRect, _win32_Edit_GetRect_cpp, controls.Edit_GetRect, controls._win32_Edit_GetRect, windowsx/Edit_GetRect
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
 - Edit_GetRect
 - windowsx/Edit_GetRect
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
 - Edit_GetRect
---

# Edit_GetRect macro

## -syntax

```cpp
void Edit_GetRect(
   HWND hwndCtl,
   RECT *lprc
);
```


## -description

Gets the formatting rectangle of an edit control. You can use this macro or send the <a href="/windows/desktop/Controls/em-getrect">EM_GETRECT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param lprc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the formatting rectangle.

## -remarks

For more information, see <a href="/windows/desktop/Controls/em-getrect">EM_GETRECT</a>.
