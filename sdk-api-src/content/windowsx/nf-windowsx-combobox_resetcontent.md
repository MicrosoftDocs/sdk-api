---
UID: NF:windowsx.ComboBox_ResetContent
title: ComboBox_ResetContent macro (windowsx.h)
description: Removes all items from the list box and edit control of a combo box. You can use this macro or send the CB_RESETCONTENT message explicitly.
helpviewer_keywords: ["ComboBox_ResetContent","ComboBox_ResetContent macro [Windows Controls]","_win32_ComboBox_ResetContent","_win32_ComboBox_ResetContent_cpp","controls.ComboBox_ResetContent","controls._win32_ComboBox_ResetContent","windowsx/ComboBox_ResetContent"]
old-location: controls\ComboBox_ResetContent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_resetcontent.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_ResetContent, ComboBox_ResetContent macro [Windows Controls], _win32_ComboBox_ResetContent, _win32_ComboBox_ResetContent_cpp, controls.ComboBox_ResetContent, controls._win32_ComboBox_ResetContent, windowsx/ComboBox_ResetContent
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
 - ComboBox_ResetContent
 - windowsx/ComboBox_ResetContent
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
 - ComboBox_ResetContent
---

# ComboBox_ResetContent macro

## -syntax

```cpp
int ComboBox_ResetContent(
   HWND hwndCtl
);
```

## -returns

Type: **int**

Always returns CB_OKAY.


## -description

Removes all items from the list box and edit control of a combo box. You can use this macro or send the <a href="/windows/desktop/Controls/cb-resetcontent">CB_RESETCONTENT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.
