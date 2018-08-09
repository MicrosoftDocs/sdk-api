---
UID: NF:windowsx.ListBox_AddItemData
title: ListBox_AddItemData macro
author: windows-sdk-content
description: Adds item data to the list box at the specified location. You can use this macro or send the LB_ADDSTRING message explicitly.
old-location: controls\ListBox_AddItemData.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_additemdata.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ListBox_AddItemData, ListBox_AddItemData macro [Windows Controls], _win32_ListBox_AddItemData, _win32_ListBox_AddItemData_cpp, controls.ListBox_AddItemData, controls._win32_ListBox_AddItemData, windowsx/ListBox_AddItemData
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
 - ListBox_AddItemData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ListBox_AddItemData macro


## -description


Adds item data to the list box at the specified location. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775181(v=VS.85).aspx">LB_ADDSTRING</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param data

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

A pointer to the item data to add.


## -remarks



Use this macro for a list box with an owner-drawn style but without the <a href="List_Box_Styles.htm">LBS_HASSTRINGS</a> style. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb775181(v=VS.85).aspx">LB_ADDSTRING</a>.
	



