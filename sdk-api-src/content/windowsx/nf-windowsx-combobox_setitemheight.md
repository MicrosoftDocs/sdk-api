---
UID: NF:windowsx.ComboBox_SetItemHeight
title: ComboBox_SetItemHeight macro (windowsx.h)
description: Sets the height of list items or the selection field in a combo box. You can use this macro or send the CB_SETITEMHEIGHT message explicitly.
helpviewer_keywords: ["ComboBox_SetItemHeight","ComboBox_SetItemHeight macro [Windows Controls]","_win32_ComboBox_SetItemHeight","_win32_ComboBox_SetItemHeight_cpp","controls.ComboBox_SetItemHeight","controls._win32_ComboBox_SetItemHeight","windowsx/ComboBox_SetItemHeight"]
old-location: controls\ComboBox_SetItemHeight.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_setitemheight.htm
ms.date: 12/05/2018
ms.keywords: ComboBox_SetItemHeight, ComboBox_SetItemHeight macro [Windows Controls], _win32_ComboBox_SetItemHeight, _win32_ComboBox_SetItemHeight_cpp, controls.ComboBox_SetItemHeight, controls._win32_ComboBox_SetItemHeight, windowsx/ComboBox_SetItemHeight
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
 - ComboBox_SetItemHeight
 - windowsx/ComboBox_SetItemHeight
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
 - ComboBox_SetItemHeight
---

# ComboBox_SetItemHeight macro


## -description

Sets the height of list items or the selection field in a combo box. You can use this macro or send the <a href="/windows/desktop/Controls/cb-setitemheight">CB_SETITEMHEIGHT</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param index

Type: <b>int</b>

The component of the combo box for which to set the height. This parameter must be –1 to set the height of the selection field. It must be zero to set the height of list items, unless the combo box has the <a href="/windows/desktop/Controls/combo-box-styles">CBS_OWNERDRAWVARIABLE</a> style. In that case, the <i>index</i> parameter is the zero-based index of a specific list item.

### -param cyItem

Type: <b>int</b>

The height in pixels.

## -remarks

For more information, see <a href="/windows/desktop/Controls/cb-setitemheight">CB_SETITEMHEIGHT</a>.