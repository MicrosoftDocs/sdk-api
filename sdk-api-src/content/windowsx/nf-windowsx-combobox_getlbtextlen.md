---
UID: NF:windowsx.ComboBox_GetLBTextLen
title: ComboBox_GetLBTextLen macro (windowsx.h)
description: Gets the length of a string in the list in a combo box. You can use this macro or send the CB_GETLBTEXTLEN message explicitly.
helpviewer_keywords: ["ComboBox_GetLBTextLen","ComboBox_GetLBTextLen macro [Windows Controls]","_win32_ComboBox_GetLBTextLen","_win32_ComboBox_GetLBTextLen_cpp","controls.ComboBox_GetLBTextLen","controls._win32_ComboBox_GetLBTextLen","windowsx/ComboBox_GetLBTextLen"]
old-location: controls\ComboBox_GetLBTextLen.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getlbtextlen.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_GetLBTextLen, ComboBox_GetLBTextLen macro [Windows Controls], _win32_ComboBox_GetLBTextLen, _win32_ComboBox_GetLBTextLen_cpp, controls.ComboBox_GetLBTextLen, controls._win32_ComboBox_GetLBTextLen, windowsx/ComboBox_GetLBTextLen
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
 - ComboBox_GetLBTextLen
 - windowsx/ComboBox_GetLBTextLen
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
 - ComboBox_GetLBTextLen
---

# ComboBox_GetLBTextLen macro

## -syntax

```cpp
int ComboBox_GetLBTextLen(
   HWND hwndCtl,
   int  index
);
```

## -returns

Type: **int**

The count of characters in the string.


## -description

Gets the length of a string in the list in a combo box.  You can use this macro or send the <a href="/windows/desktop/Controls/cb-getlbtextlen">CB_GETLBTEXTLEN</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param index

Type: <b>int</b>

The zero-based index of the item.

## -remarks

For more information, see <a href="/windows/desktop/Controls/cb-getlbtextlen">CB_GETLBTEXTLEN</a>.
