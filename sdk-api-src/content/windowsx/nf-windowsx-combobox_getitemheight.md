---
UID: NF:windowsx.ComboBox_GetItemHeight
title: ComboBox_GetItemHeight macro (windowsx.h)
description: Retrieves the height of list items in a combo box. You can use this macro or send the CB_GETITEMHEIGHT message explicitly.
helpviewer_keywords: ["ComboBox_GetItemHeight","ComboBox_GetItemHeight macro [Windows Controls]","_win32_ComboBox_GetItemHeight","_win32_ComboBox_GetItemHeight_cpp","controls.ComboBox_GetItemHeight","controls._win32_ComboBox_GetItemHeight","windowsx/ComboBox_GetItemHeight"]
old-location: controls\ComboBox_GetItemHeight.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getitemheight.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_GetItemHeight, ComboBox_GetItemHeight macro [Windows Controls], _win32_ComboBox_GetItemHeight, _win32_ComboBox_GetItemHeight_cpp, controls.ComboBox_GetItemHeight, controls._win32_ComboBox_GetItemHeight, windowsx/ComboBox_GetItemHeight
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
 - ComboBox_GetItemHeight
 - windowsx/ComboBox_GetItemHeight
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
 - ComboBox_GetItemHeight
---

# ComboBox_GetItemHeight macro

## -syntax

```cpp
int ComboBox_GetItemHeight(
   HWND hwndCtl
);
```

## -returns

Type: **int**

The height, in pixels, of the list items in a combo box.


## -description

Retrieves the height of list items in a combo box. You can use this macro or send the <a href="/windows/desktop/Controls/cb-getitemheight">CB_GETITEMHEIGHT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

## -remarks

This macro passes zero as the <i>wParam</i> member of <a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a>. For more information, see <a href="/windows/desktop/Controls/cb-getitemheight">CB_GETITEMHEIGHT</a>.
