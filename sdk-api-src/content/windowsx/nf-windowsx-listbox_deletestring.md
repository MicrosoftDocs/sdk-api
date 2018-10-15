---
UID: NF:windowsx.ListBox_DeleteString
title: ListBox_DeleteString macro
author: windows-sdk-content
description: Deletes the item at the specified location in a list box. You can use this macro or send the LB_DELETESTRING message explicitly.
old-location: controls\ListBox_DeleteString.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_deletestring.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: ListBox_DeleteString, ListBox_DeleteString macro [Windows Controls], _win32_ListBox_DeleteString, _win32_ListBox_DeleteString_cpp, controls.ListBox_DeleteString, controls._win32_ListBox_DeleteString, windowsx/ListBox_DeleteString
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
 - ListBox_DeleteString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListBox_DeleteString macro


## -description


Deletes the item at the specified location in a list box. You can use this macro or send the <a href="https://msdn.microsoft.com/3f360e07-b70d-4bfc-89d4-18d3b18b0fcf">LB_DELETESTRING</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item to delete.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/3f360e07-b70d-4bfc-89d4-18d3b18b0fcf">LB_DELETESTRING</a>




