---
UID: NF:windowsx.ListBox_SetCurSel
title: ListBox_SetCurSel macro
author: windows-sdk-content
description: Sets the currently selected item in a single-selection list box. You can use this macro or send the LB_SETCURSEL message explicitly.
old-location: controls\ListBox_SetCurSel.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_setcursel.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ListBox_SetCurSel, ListBox_SetCurSel macro [Windows Controls], _win32_ListBox_SetCurSel, _win32_ListBox_SetCurSel_cpp, controls.ListBox_SetCurSel, controls._win32_ListBox_SetCurSel, windowsx/ListBox_SetCurSel
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
 - ListBox_SetCurSel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ListBox_SetCurSel macro


## -description


Sets the currently selected item in a single-selection list box. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761342(v=VS.85).aspx">LB_SETCURSEL</a> message explicitly.




## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item to select, or –1 to clear the selection.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb761342(v=VS.85).aspx">LB_SETCURSEL</a>.



