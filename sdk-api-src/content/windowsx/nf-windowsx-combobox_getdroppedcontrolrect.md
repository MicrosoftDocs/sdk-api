---
UID: NF:windowsx.ComboBox_GetDroppedControlRect
title: ComboBox_GetDroppedControlRect macro (windowsx.h)
description: Retrieves the screen coordinates of a combo box in its dropped-down state. You can use this macro or send the CB_GETDROPPEDCONTROLRECT message explicitly.
helpviewer_keywords: ["ComboBox_GetDroppedControlRect","ComboBox_GetDroppedControlRect macro [Windows Controls]","_win32_ComboBox_GetDroppedControlRect","_win32_ComboBox_GetDroppedControlRect_cpp","controls.ComboBox_GetDroppedControlRect","controls._win32_ComboBox_GetDroppedControlRect","windowsx/ComboBox_GetDroppedControlRect"]
old-location: controls\ComboBox_GetDroppedControlRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getdroppedcontrolrect.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_GetDroppedControlRect, ComboBox_GetDroppedControlRect macro [Windows Controls], _win32_ComboBox_GetDroppedControlRect, _win32_ComboBox_GetDroppedControlRect_cpp, controls.ComboBox_GetDroppedControlRect, controls._win32_ComboBox_GetDroppedControlRect, windowsx/ComboBox_GetDroppedControlRect
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
 - ComboBox_GetDroppedControlRect
 - windowsx/ComboBox_GetDroppedControlRect
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
 - ComboBox_GetDroppedControlRect
---

# ComboBox_GetDroppedControlRect macro

## -syntax

```cpp
void ComboBox_GetDroppedControlRect(
   HWND hwndCtl,
   RECT *lprc
);
```


## -description

Retrieves the screen coordinates of a combo box in its dropped-down state. You can use this macro or send the <a href="/windows/desktop/Controls/cb-getdroppedcontrolrect">CB_GETDROPPEDCONTROLRECT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param lprc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the coordinates of the combo box in its dropped-down state.
