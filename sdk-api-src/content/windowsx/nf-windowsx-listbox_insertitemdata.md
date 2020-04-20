---
UID: NF:windowsx.ListBox_InsertItemData
title: ListBox_InsertItemData macro (windowsx.h)
description: Inserts item data to a list box at the specified location. You can use this macro or send the LB_INSERTSTRING message explicitly.helpviewer_keywords: ["ListBox_InsertItemData","ListBox_InsertItemData macro [Windows Controls]","_win32_ListBox_InsertItemData","_win32_ListBox_InsertItemData_cpp","controls.ListBox_InsertItemData","controls._win32_ListBox_InsertItemData","windowsx/ListBox_InsertItemData"]
old-location: controls\ListBox_InsertItemData.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_insertitemdata.htm
ms.date: 12/05/2018
ms.keywords: ListBox_InsertItemData, ListBox_InsertItemData macro [Windows Controls], _win32_ListBox_InsertItemData, _win32_ListBox_InsertItemData_cpp, controls.ListBox_InsertItemData, controls._win32_ListBox_InsertItemData, windowsx/ListBox_InsertItemData
f1_keywords:
- windowsx/ListBox_InsertItemData
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
- ListBox_InsertItemData
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListBox_InsertItemData macro


## -description


Inserts item data to a list box at the specified location. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lb-insertstring">LB_INSERTSTRING</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index in the list at which to insert the item data, or –1 to add it to the end of the list.


### -param data

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

A pointer to the item data to insert.


## -remarks



Use this macro for a list box with an owner-drawn style but without the <a href="https://docs.microsoft.com/windows/desktop/Controls/list-box-styles">LBS_HASSTRINGS</a> style. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/lb-insertstring">LB_INSERTSTRING</a>.
	



