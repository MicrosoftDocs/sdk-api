---
UID: NF:windowsx.ComboBox_LimitText
title: ComboBox_LimitText macro (windowsx.h)
description: Limits the length of the text the user may type into the edit control of a combo box. You can use this macro or send the CB_LIMITTEXT message explicitly.
helpviewer_keywords: ["ComboBox_LimitText","ComboBox_LimitText macro [Windows Controls]","_win32_ComboBox_LimitText","_win32_ComboBox_LimitText_cpp","controls.ComboBox_LimitText","controls._win32_ComboBox_LimitText","windowsx/ComboBox_LimitText"]
old-location: controls\ComboBox_LimitText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\combobox_limittext.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_LimitText, ComboBox_LimitText macro [Windows Controls], _win32_ComboBox_LimitText, _win32_ComboBox_LimitText_cpp, controls.ComboBox_LimitText, controls._win32_ComboBox_LimitText, windowsx/ComboBox_LimitText
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
 - ComboBox_LimitText
 - windowsx/ComboBox_LimitText
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
 - ComboBox_LimitText
---

# ComboBox_LimitText macro

## -syntax

```cpp
int ComboBox_LimitText(
   HWND hwndCtl,
   int  cchLimit
);
```

## -returns

Type: **int**

Always returns nonzero.


## -description

Limits the length of the text the user may type into the edit control of a combo box. You can use this macro or send the <a href="/windows/desktop/Controls/cb-limittext">CB_LIMITTEXT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param cchLimit

Type: <b>int</b>

The maximum number of characters.

## -remarks

For more information, see <a href="/windows/desktop/Controls/cb-limittext">CB_LIMITTEXT</a>.
