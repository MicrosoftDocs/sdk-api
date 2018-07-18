---
UID: NF:windowsx.ListBox_GetSel
title: ListBox_GetSel macro
author: windows-sdk-content
description: Gets the selection state of an item. You can use this macro or send the LB_GETSEL message explicitly.
old-location: controls\ListBox_GetSel.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_getsel.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ListBox_GetSel, ListBox_GetSel macro [Windows Controls], _win32_ListBox_GetSel, _win32_ListBox_GetSel_cpp, controls.ListBox_GetSel, controls._win32_ListBox_GetSel, windowsx/ListBox_GetSel
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
 - ListBox_GetSel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ListBox_GetSel macro


## -description


Gets the selection state of an item. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb775212(v=VS.85).aspx">LB_GETSEL</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/library/Bb775212(v=VS.85).aspx">LB_GETSEL</a>




