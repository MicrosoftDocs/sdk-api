---
UID: NF:windowsx.ListBox_GetItemData
title: ListBox_GetItemData macro
author: windows-sdk-content
description: Gets the application-defined value associated with the specified list box item. You can use this macro or send the LB_GETITEMDATA message explicitly.
old-location: controls\ListBox_GetItemData.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_getitemdata.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ListBox_GetItemData, ListBox_GetItemData macro [Windows Controls], _win32_ListBox_GetItemData, _win32_ListBox_GetItemData_cpp, controls.ListBox_GetItemData, controls._win32_ListBox_GetItemData, windowsx/ListBox_GetItemData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: windowsx.h
req.include-header: 
req.redist: 
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
 - ListBox_GetItemData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ListBox_GetItemData macro


## -description


Gets the application-defined value associated with the specified list box item. You can use this macro or send the <a href="https://msdn.microsoft.com/3a3f7fa5-ce04-4e95-86e1-5c7de796d1b6">LB_GETITEMDATA</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item.

