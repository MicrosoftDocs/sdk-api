---
UID: NF:windowsx.ComboBox_GetTextLength
title: ComboBox_GetTextLength macro (windowsx.h)
description: Gets the number of characters in the text of a combo box.
helpviewer_keywords: ["ComboBox_GetTextLength","ComboBox_GetTextLength macro [Windows Controls]","_win32_ComboBox_GetTextLength","_win32_ComboBox_GetTextLength_cpp","controls.ComboBox_GetTextLength","controls._win32_ComboBox_GetTextLength","windowsx/ComboBox_GetTextLength"]
old-location: controls\ComboBox_GetTextLength.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\combobox_gettextlength.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_GetTextLength, ComboBox_GetTextLength macro [Windows Controls], _win32_ComboBox_GetTextLength, _win32_ComboBox_GetTextLength_cpp, controls.ComboBox_GetTextLength, controls._win32_ComboBox_GetTextLength, windowsx/ComboBox_GetTextLength
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
 - ComboBox_GetTextLength
 - windowsx/ComboBox_GetTextLength
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
 - ComboBox_GetTextLength
---

# ComboBox_GetTextLength macro

## -syntax

```cpp
int ComboBox_GetTextLength(
   HWND hwndCtl
);
```

## -returns

Type: **int**

The length, in characters, of the text.


## -description

Gets the number of characters in the text of a combo box.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

## -remarks

The macro expands to a call to <a href="/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha">GetWindowTextLength</a>.
