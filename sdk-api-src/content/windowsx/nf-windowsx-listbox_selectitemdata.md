---
UID: NF:windowsx.ListBox_SelectItemData
title: ListBox_SelectItemData macro
author: windows-sdk-content
description: Searches a list box for an item that has the specified item data. If a matching item is found, the item is selected. You can use this macro or send the LB_SELECTSTRING message explicitly.
old-location: controls\ListBox_SelectItemData.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_selectitemdata.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ListBox_SelectItemData, ListBox_SelectItemData macro [Windows Controls], _win32_ListBox_SelectItemData, _win32_ListBox_SelectItemData_cpp, controls.ListBox_SelectItemData, controls._win32_ListBox_SelectItemData, windowsx/ListBox_SelectItemData
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ListBox_SelectItemData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListBox_SelectItemData macro


## -description


Searches a list box for an item that has the specified item data. If a matching item is found, the item is selected. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761327(v=VS.85).aspx">LB_SELECTSTRING</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param indexStart

Type: <b>int</b>

The zero-based index of the item before the first item to be searched. When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the <i>indexStart</i> parameter. If <i>indexStart</i>  is –1, the entire list box is searched from the beginning.


### -param data

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

The item data to find.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb761327(v=VS.85).aspx">LB_SELECTSTRING</a>.
	



