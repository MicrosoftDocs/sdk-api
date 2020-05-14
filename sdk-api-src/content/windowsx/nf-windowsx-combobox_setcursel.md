---
UID: NF:windowsx.ComboBox_SetCurSel
title: ComboBox_SetCurSel macro (windowsx.h)
description: Sets the currently selected item in a combo box. You can use this macro or send the CB_SETCURSEL message explicitly.helpviewer_keywords: ["ComboBox_SetCurSel","ComboBox_SetCurSel macro [Windows Controls]","_win32_ComboBox_SetCurSel","_win32_ComboBox_SetCurSel_cpp","controls.ComboBox_SetCurSel","controls._win32_ComboBox_SetCurSel","windowsx/ComboBox_SetCurSel"]
old-location: controls\ComboBox_SetCurSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_setcursel.htm
ms.date: 12/05/2018
ms.keywords: ComboBox_SetCurSel, ComboBox_SetCurSel macro [Windows Controls], _win32_ComboBox_SetCurSel, _win32_ComboBox_SetCurSel_cpp, controls.ComboBox_SetCurSel, controls._win32_ComboBox_SetCurSel, windowsx/ComboBox_SetCurSel
f1_keywords:
- windowsx/ComboBox_SetCurSel
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Windowsx.h
api_name:
- ComboBox_SetCurSel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ComboBox_SetCurSel macro


## -description


Sets the currently selected item in a combo box. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/cb-setcursel">CB_SETCURSEL</a> message explicitly.




## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item to select, or –1 to clear the selection.

