---
UID: NF:windowsx.ListBox_SetCaretIndex
title: ListBox_SetCaretIndex macro
author: windows-sdk-content
description: Sets the focus rectangle to the item at the specified index in a multiple-selection list box. If the item is not visible, it is scrolled into view. You can use this macro or send the LB_SETCARETINDEX message explicitly.
old-location: controls\ListBox_SetCaretIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_setcaretindex.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ListBox_SetCaretIndex, ListBox_SetCaretIndex macro [Windows Controls], _win32_ListBox_SetCaretIndex, _win32_ListBox_SetCaretIndex_cpp, controls.ListBox_SetCaretIndex, controls._win32_ListBox_SetCaretIndex, windowsx/ListBox_SetCaretIndex
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
 - ListBox_SetCaretIndex
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListBox_SetCaretIndex macro


## -description


Sets the focus rectangle to the item at the specified index in a multiple-selection list box. If the item is not visible, it is scrolled into view. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761336(v=VS.85).aspx">LB_SETCARETINDEX</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

 the zero-based index of the list box item that is to receive the focus rectangle. 


## -remarks



The contents of the list box are scrolled till the item is fully visible.

For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb761336(v=VS.85).aspx">LB_SETCARETINDEX</a>.



