---
UID: NF:windowsx.ListBox_SetSel
title: ListBox_SetSel macro
author: windows-sdk-content
description: Selects or deselects an item in a multiple-selection list box. You can use this macro or send the LB_SETSEL message explicitly.
old-location: controls\ListBox_SetSel.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_setsel.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ListBox_SetSel, ListBox_SetSel macro [Windows Controls], _win32_ListBox_SetSel, _win32_ListBox_SetSel_cpp, controls.ListBox_SetSel, controls._win32_ListBox_SetSel, windowsx/ListBox_SetSel
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
 - ListBox_SetSel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ListBox_SetSel macro


## -description


Selects or deselects an item in a multiple-selection list box. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb761352(v=VS.85).aspx">LB_SETSEL</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param fSelect

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> to select the item, or <b>FALSE</b> to deselect it.


### -param index

Type: <b>int</b>

The zero-based index of the item.

