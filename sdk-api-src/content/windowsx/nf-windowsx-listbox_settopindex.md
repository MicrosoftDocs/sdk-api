---
UID: NF:windowsx.ListBox_SetTopIndex
title: ListBox_SetTopIndex macro (windowsx.h)
description: Ensures that the specified item in a list box is visible. You can use this macro or send the LB_SETTOPINDEX message explicitly.
helpviewer_keywords: ["ListBox_SetTopIndex","ListBox_SetTopIndex macro [Windows Controls]","_win32_ListBox_SetTopIndex","_win32_ListBox_SetTopIndex_cpp","controls.ListBox_SetTopIndex","controls._win32_ListBox_SetTopIndex","windowsx/ListBox_SetTopIndex"]
old-location: controls\ListBox_SetTopIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_settopindex.htm
ms.date: 12/05/2018
ms.keywords: ListBox_SetTopIndex, ListBox_SetTopIndex macro [Windows Controls], _win32_ListBox_SetTopIndex, _win32_ListBox_SetTopIndex_cpp, controls.ListBox_SetTopIndex, controls._win32_ListBox_SetTopIndex, windowsx/ListBox_SetTopIndex
f1_keywords:
- windowsx/ListBox_SetTopIndex
dev_langs:
- c++
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
- ListBox_SetTopIndex
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListBox_SetTopIndex macro


## -description


Ensures that the specified item in a list box is visible. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/controls/lb-settopindex">LB_SETTOPINDEX</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param indexTop

Type: <b>int</b>

The zero-based index of the item to put at the top of the visible part of the list.


## -remarks



The list box contents are scrolled so that either the specified item appears at the top of the list box or the maximum scroll range has been reached.



