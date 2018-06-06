---
UID: NF:windowsx.ComboBox_SelectItemData
title: ComboBox_SelectItemData macro
author: windows-sdk-content
description: Searches a list in a combo box for an item that has the specified item data. If a matching item is found, the item is selected. You can use this macro or send the CB_SELECTSTRING message explicitly.
old-location: controls\ComboBox_SelectItemData.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_selectitemdata.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ComboBox_SelectItemData, ComboBox_SelectItemData macro [Windows Controls], _win32_ComboBox_SelectItemData, _win32_ComboBox_SelectItemData_cpp, controls.ComboBox_SelectItemData, controls._win32_ComboBox_SelectItemData, windowsx/ComboBox_SelectItemData
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
 - ComboBox_SelectItemData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ComboBox_SelectItemData macro


## -description


Searches a list in a combo box for an item that has the specified item data. If a matching item is found, the item is selected. You can use this macro or send the <a href="https://msdn.microsoft.com/c08dff72-7e44-40ed-8b64-513359292829">CB_SELECTSTRING</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param indexStart

Type: <b>int</b>

The zero-based index of the item before the first item to be searched. When the search reaches the bottom of the list, it continues searching from the top of the list back to the item specified by the <i>indexStart</i> parameter. If <i>indexStart</i>  is –1, the entire list is searched from the beginning.


### -param data

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

The item data to find.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/c08dff72-7e44-40ed-8b64-513359292829">CB_SELECTSTRING</a>.
	



