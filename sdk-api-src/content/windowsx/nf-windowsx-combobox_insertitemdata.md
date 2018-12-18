---
UID: NF:windowsx.ComboBox_InsertItemData
title: ComboBox_InsertItemData macro
author: windows-sdk-content
description: Inserts item data in a list in a combo box at the specified location. You can use this macro or send the CB_INSERTSTRING message explicitly.
old-location: controls\ComboBox_InsertItemData.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_insertitemdata.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ComboBox_InsertItemData, ComboBox_InsertItemData macro [Windows Controls], _win32_ComboBox_InsertItemData, _win32_ComboBox_InsertItemData_cpp, controls.ComboBox_InsertItemData, controls._win32_ComboBox_InsertItemData, windowsx/ComboBox_InsertItemData
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
 - ComboBox_InsertItemData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ComboBox_InsertItemData macro


## -description


Inserts item data in a list in a combo box at the specified location. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775875(v=VS.85).aspx">CB_INSERTSTRING</a> message explicitly.


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



Use this macro for a list in a combo box with an owner-drawn style but without the <a href="https://msdn.microsoft.com/en-us/library/Bb775796(v=VS.85).aspx">CBS_HASSTRINGS</a> style. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb775875(v=VS.85).aspx">CB_INSERTSTRING</a>.
	



