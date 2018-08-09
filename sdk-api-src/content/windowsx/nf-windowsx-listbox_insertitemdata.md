---
UID: NF:windowsx.ListBox_InsertItemData
title: ListBox_InsertItemData macro
author: windows-sdk-content
description: Inserts item data to a list box at the specified location. You can use this macro or send the LB_INSERTSTRING message explicitly.
old-location: controls\ListBox_InsertItemData.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_insertitemdata.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ListBox_InsertItemData, ListBox_InsertItemData macro [Windows Controls], _win32_ListBox_InsertItemData, _win32_ListBox_InsertItemData_cpp, controls.ListBox_InsertItemData, controls._win32_ListBox_InsertItemData, windowsx/ListBox_InsertItemData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
tech.root: 
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - ListBox_InsertItemData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ListBox_InsertItemData macro


## -description


Inserts item data to a list box at the specified location. You can use this macro or send the <a href="https://msdn.microsoft.com/dfaa742d-2f42-4485-aed5-cda8ca9ba66c">LB_INSERTSTRING</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index in the list at which to insert the item data, or –1 to add it to the end of the list.


### -param data

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

A pointer to the item data to insert.


## -remarks



Use this macro for a list box with an owner-drawn style but without the <a href="List_Box_Styles.htm">LBS_HASSTRINGS</a> style. For more information, see <a href="https://msdn.microsoft.com/dfaa742d-2f42-4485-aed5-cda8ca9ba66c">LB_INSERTSTRING</a>.
	



