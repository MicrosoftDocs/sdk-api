---
UID: NF:windowsx.ComboBox_GetLBText
title: ComboBox_GetLBText macro (windowsx.h)
description: Gets a string from a list in a combo box. You can use this macro or send the CB_GETLBTEXT message explicitly.
helpviewer_keywords: ["ComboBox_GetLBText","ComboBox_GetLBText macro [Windows Controls]","_win32_ComboBox_GetLBText","_win32_ComboBox_GetLBText_cpp","controls.ComboBox_GetLBText","controls._win32_ComboBox_GetLBText","windowsx/ComboBox_GetLBText"]
old-location: controls\ComboBox_GetLBText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getlbtext.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_GetLBText, ComboBox_GetLBText macro [Windows Controls], _win32_ComboBox_GetLBText, _win32_ComboBox_GetLBText_cpp, controls.ComboBox_GetLBText, controls._win32_ComboBox_GetLBText, windowsx/ComboBox_GetLBText
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
 - ComboBox_GetLBText
 - windowsx/ComboBox_GetLBText
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
 - ComboBox_GetLBText
---

# ComboBox_GetLBText macro

## -syntax

```cpp
int ComboBox_GetLBText(
   HWND    hwndCtl,
   int     index,
   LPCTSTR lpszBuffer
);
```

## -returns

Type: **int**

The count of characters in the string, excluding the terminating null character. If <i>index</i> does not specify a valid item, the return value is CB_ERR.


## -description

Gets a string from a list in a combo box. You can use this macro or send the <a href="/windows/desktop/Controls/cb-getlbtext">CB_GETLBTEXT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param index

Type: <b>int</b>

The zero-based index of the item.

### -param lpszBuffer

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

A pointer to the buffer that will receive the string. The buffer must have sufficient space for the string and a terminating null character. Before allocating the buffer, you can call <a href="/windows/desktop/api/windowsx/nf-windowsx-combobox_getlbtextlen">ComboBox_GetLBTextLen</a> to retrieve the length of the string.

## -remarks

For more information, see <a href="/windows/desktop/Controls/cb-getlbtext">CB_GETLBTEXT</a>.
