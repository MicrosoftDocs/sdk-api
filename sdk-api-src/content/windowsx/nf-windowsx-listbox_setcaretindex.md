---
UID: NF:windowsx.ListBox_SetCaretIndex
title: ListBox_SetCaretIndex macro (windowsx.h)
description: Sets the focus rectangle to the item at the specified index in a multiple-selection list box. If the item is not visible, it is scrolled into view. You can use this macro or send the LB_SETCARETINDEX message explicitly.
helpviewer_keywords: ["ListBox_SetCaretIndex","ListBox_SetCaretIndex macro [Windows Controls]","_win32_ListBox_SetCaretIndex","_win32_ListBox_SetCaretIndex_cpp","controls.ListBox_SetCaretIndex","controls._win32_ListBox_SetCaretIndex","windowsx/ListBox_SetCaretIndex"]
old-location: controls\ListBox_SetCaretIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_setcaretindex.htm
ms.date: 12/05/2018
ms.keywords: ListBox_SetCaretIndex, ListBox_SetCaretIndex macro [Windows Controls], _win32_ListBox_SetCaretIndex, _win32_ListBox_SetCaretIndex_cpp, controls.ListBox_SetCaretIndex, controls._win32_ListBox_SetCaretIndex, windowsx/ListBox_SetCaretIndex
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ListBox_SetCaretIndex
 - windowsx/ListBox_SetCaretIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - ListBox_SetCaretIndex
---

# ListBox_SetCaretIndex macro


## -description

Sets the focus rectangle to the item at the specified index in a multiple-selection list box. If the item is not visible, it is scrolled into view. You can use this macro or send the <a href="/windows/desktop/controls/lb-setcaretindex">LB_SETCARETINDEX</a> message explicitly.

## -parameters

### -param hwndCtl

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.

### -param index

Type: <b>int</b>

 the zero-based index of the list box item that is to receive the focus rectangle.

## -remarks

The contents of the list box are scrolled till the item is fully visible.

For more information, see <a href="/windows/desktop/controls/lb-setcaretindex">LB_SETCARETINDEX</a>.