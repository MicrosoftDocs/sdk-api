---
UID: NF:commctrl.ComboBox_GetMinVisible
title: ComboBox_GetMinVisible macro (commctrl.h)
description: Gets the minimum number of visible items in the drop-down list of a combo box.
helpviewer_keywords: ["ComboBox_GetMinVisible","ComboBox_GetMinVisible macro [Windows Controls]","_win32_ComboBox_GetMinVisible","_win32_ComboBox_GetMinVisible_cpp","commctrl/ComboBox_GetMinVisible","controls.ComboBox_GetMinVisible","controls._win32_ComboBox_GetMinVisible"]
old-location: controls\ComboBox_GetMinVisible.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getminvisible.htm
ms.date: 10/21/2024
ms.keywords: ComboBox_GetMinVisible, ComboBox_GetMinVisible macro [Windows Controls], _win32_ComboBox_GetMinVisible, _win32_ComboBox_GetMinVisible_cpp, commctrl/ComboBox_GetMinVisible, controls.ComboBox_GetMinVisible, controls._win32_ComboBox_GetMinVisible
req.header: commctrl.h
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
 - ComboBox_GetMinVisible
 - commctrl/ComboBox_GetMinVisible
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ComboBox_GetMinVisible
---

# ComboBox_GetMinVisible macro

## -syntax

```cpp
INT ComboBox_GetMinVisible(
   HWND hwnd
);
```

## -returns

Type: **[INT](/windows/desktop/winprog/windows-data-types)**

The return value is the minimum number of visible items.


## -description

Gets the minimum number of visible items in the drop-down list of a combo box.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Specifies the combo box.

## -remarks

When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar. 

To use <b>ComboBox_GetMinVisible</b>, the application must specify comctl32.dll version 6 in the manifest. For more information, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.

## -see-also

<a href="/windows/desktop/Controls/cb-getminvisible">CB_GETMINVISIBLE</a>
