---
UID: NF:windowsx.ComboBox_GetItemData
title: ComboBox_GetItemData macro (windowsx.h)
description: Gets the application-defined value associated with the specified list item in a combo box. You can use this macro or send the CB_GETITEMDATA message explicitly.
helpviewer_keywords: ["ComboBox_GetItemData","ComboBox_GetItemData macro [Windows Controls]","_win32_ComboBox_GetItemData","_win32_ComboBox_GetItemData_cpp","controls.ComboBox_GetItemData","controls._win32_ComboBox_GetItemData","windowsx/ComboBox_GetItemData"]
old-location: controls\ComboBox_GetItemData.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getitemdata.htm
ms.date: 12/05/2018
ms.keywords: ComboBox_GetItemData, ComboBox_GetItemData macro [Windows Controls], _win32_ComboBox_GetItemData, _win32_ComboBox_GetItemData_cpp, controls.ComboBox_GetItemData, controls._win32_ComboBox_GetItemData, windowsx/ComboBox_GetItemData
f1_keywords:
- windowsx/ComboBox_GetItemData
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
- ComboBox_GetItemData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ComboBox_GetItemData macro


## -description


Gets the application-defined value associated with the specified list item in a combo box. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/cb-getitemdata">CB_GETITEMDATA</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item.

