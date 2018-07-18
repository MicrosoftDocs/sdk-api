---
UID: NF:windowsx.ComboBox_InsertItemData
title: ComboBox_InsertItemData macro
author: windows-sdk-content
description: Inserts item data in a list in a combo box at the specified location. You can use this macro or send the CB_INSERTSTRING message explicitly.
old-location: controls\ComboBox_InsertItemData.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_insertitemdata.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ComboBox_InsertItemData, ComboBox_InsertItemData macro [Windows Controls], _win32_ComboBox_InsertItemData, _win32_ComboBox_InsertItemData_cpp, controls.ComboBox_InsertItemData, controls._win32_ComboBox_InsertItemData, windowsx/ComboBox_InsertItemData
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
 - ComboBox_InsertItemData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ComboBox_InsertItemData macro


## -description


Inserts item data in a list in a combo box at the specified location. You can use this macro or send the <a href="https://msdn.microsoft.com/b9067b4e-afca-4c78-9ca2-c717b99c7459">CB_INSERTSTRING</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index in the list at which to insert the item data, or –1 to add it to the end of the list.


### -param data

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

The item data to insert.


## -remarks



Use this macro for a list in a combo box with an owner-drawn style but without the <a href="Combo_Box_Styles.htm">CBS_HASSTRINGS</a> style. For more information, see <a href="https://msdn.microsoft.com/b9067b4e-afca-4c78-9ca2-c717b99c7459">CB_INSERTSTRING</a>.
	



