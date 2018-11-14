---
UID: NF:windowsx.ListBox_SetItemData
title: ListBox_SetItemData macro
author: windows-sdk-content
description: Sets the application-defined value associated with the specified list box item. You can use this macro or send the LB_SETITEMDATA message explicitly.
old-location: controls\ListBox_SetItemData.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_setitemdata.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ListBox_SetItemData, ListBox_SetItemData macro [Windows Controls], _win32_ListBox_SetItemData, _win32_ListBox_SetItemData_cpp, controls.ListBox_SetItemData, controls._win32_ListBox_SetItemData, windowsx/ListBox_SetItemData
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
 - ListBox_SetItemData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- windowsx.h
: 
- ListBox_SetItemData
: 
---

# ListBox_SetItemData macro


## -description


Sets the application-defined value associated with the specified list box item. You can use this macro or send the <a href="https://msdn.microsoft.com/df974fa2-114a-43ef-b0ac-0451c31d95cd">LB_SETITEMDATA</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item.


### -param data

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

The item data to set.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/df974fa2-114a-43ef-b0ac-0451c31d95cd">LB_SETITEMDATA</a>.
	



