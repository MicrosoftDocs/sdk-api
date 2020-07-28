---
UID: NF:windowsx.ComboBox_AddItemData
title: ComboBox_AddItemData macro (windowsx.h)
description: Adds item data to the list in a combo box at the specified location. You can use this macro or send the CB_ADDSTRING message explicitly.
helpviewer_keywords: ["ComboBox_AddItemData","ComboBox_AddItemData macro [Windows Controls]","_win32_ComboBox_AddItemData","_win32_ComboBox_AddItemData_cpp","controls.ComboBox_AddItemData","controls._win32_ComboBox_AddItemData","windowsx/ComboBox_AddItemData"]
old-location: controls\ComboBox_AddItemData.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_additemdata.htm
ms.date: 12/05/2018
ms.keywords: ComboBox_AddItemData, ComboBox_AddItemData macro [Windows Controls], _win32_ComboBox_AddItemData, _win32_ComboBox_AddItemData_cpp, controls.ComboBox_AddItemData, controls._win32_ComboBox_AddItemData, windowsx/ComboBox_AddItemData
f1_keywords:
- windowsx/ComboBox_AddItemData
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
- ComboBox_AddItemData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ComboBox_AddItemData macro


## -description


Adds item data to the list in a combo box at the specified location. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/cb-addstring">CB_ADDSTRING</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param data

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

A pointer to the item data to add.


## -remarks



Use this macro for a list in a combo box with an owner-drawn style but without the <a href="https://docs.microsoft.com/windows/desktop/Controls/combo-box-styles">CBS_HASSTRINGS</a> style. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cb-addstring">CB_ADDSTRING</a>.
	



