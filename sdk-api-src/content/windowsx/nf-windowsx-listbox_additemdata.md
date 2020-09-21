---
UID: NF:windowsx.ListBox_AddItemData
title: ListBox_AddItemData macro (windowsx.h)
description: Adds item data to the list box at the specified location. You can use this macro or send the LB_ADDSTRING message explicitly.
helpviewer_keywords: ["ListBox_AddItemData","ListBox_AddItemData macro [Windows Controls]","_win32_ListBox_AddItemData","_win32_ListBox_AddItemData_cpp","controls.ListBox_AddItemData","controls._win32_ListBox_AddItemData","windowsx/ListBox_AddItemData"]
old-location: controls\ListBox_AddItemData.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_additemdata.htm
ms.date: 12/05/2018
ms.keywords: ListBox_AddItemData, ListBox_AddItemData macro [Windows Controls], _win32_ListBox_AddItemData, _win32_ListBox_AddItemData_cpp, controls.ListBox_AddItemData, controls._win32_ListBox_AddItemData, windowsx/ListBox_AddItemData
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
 - ListBox_AddItemData
 - windowsx/ListBox_AddItemData
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
 - ListBox_AddItemData
---

# ListBox_AddItemData macro


## -description

Adds item data to the list box at the specified location. You can use this macro or send the <a href="/windows/desktop/Controls/lb-addstring">LB_ADDSTRING</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param data

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

A pointer to the item data to add.

## -remarks

Use this macro for a list box with an owner-drawn style but without the <a href="/windows/desktop/Controls/list-box-styles">LBS_HASSTRINGS</a> style. For more information, see <a href="/windows/desktop/Controls/lb-addstring">LB_ADDSTRING</a>.