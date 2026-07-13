---
UID: NF:windowsx.ComboBox_GetCount
title: ComboBox_GetCount macro (windowsx.h)
description: Gets the number of items in the list box of a combo box. You can use this macro or send the CB_GETCOUNT message explicitly.
helpviewer_keywords: ["ComboBox_GetCount","ComboBox_GetCount macro [Windows Controls]","_win32_ComboBox_GetCount","_win32_ComboBox_GetCount_cpp","controls.ComboBox_GetCount","controls._win32_ComboBox_GetCount","windowsx/ComboBox_GetCount"]
old-location: controls\ComboBox_GetCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getcount.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_GetCount, ComboBox_GetCount macro [Windows Controls], _win32_ComboBox_GetCount, _win32_ComboBox_GetCount_cpp, controls.ComboBox_GetCount, controls._win32_ComboBox_GetCount, windowsx/ComboBox_GetCount
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
 - ComboBox_GetCount
 - windowsx/ComboBox_GetCount
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
 - ComboBox_GetCount
---

# ComboBox_GetCount macro

## -syntax

```cpp
int ComboBox_GetCount(
   HWND hwndCtl
);
```

## -returns

Type: **int**

The number of items.


## -description

Gets the number of items in the list box of a combo box. You can use this macro or send the <a href="/windows/desktop/Controls/cb-getcount">CB_GETCOUNT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.
