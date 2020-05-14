---
UID: NF:windowsx.ListBox_GetItemHeight
title: ListBox_GetItemHeight macro (windowsx.h)
description: Retrieves the height of items in a list box.helpviewer_keywords: ["ListBox_GetItemHeight","ListBox_GetItemHeight macro [Windows Controls]","_win32_ListBox_GetItemHeight","_win32_ListBox_GetItemHeight_cpp","controls.ListBox_GetItemHeight","controls._win32_ListBox_GetItemHeight","windowsx/ListBox_GetItemHeight"]
old-location: controls\ListBox_GetItemHeight.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_getitemheight.htm
ms.date: 12/05/2018
ms.keywords: ListBox_GetItemHeight, ListBox_GetItemHeight macro [Windows Controls], _win32_ListBox_GetItemHeight, _win32_ListBox_GetItemHeight_cpp, controls.ListBox_GetItemHeight, controls._win32_ListBox_GetItemHeight, windowsx/ListBox_GetItemHeight
f1_keywords:
- windowsx/ListBox_GetItemHeight
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
- ListBox_GetItemHeight
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListBox_GetItemHeight macro


## -description


Retrieves the height of items in a list box. If the list box has the <a href="https://docs.microsoft.com/windows/desktop/Controls/list-box-styles">LBS_OWNERDRAWVARIABLE</a> style, this macro gets the height of the specified item; otherwise, it gets the height of all items. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lb-getitemheight">LB_GETITEMHEIGHT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item. If the list box does not have the <a href="https://docs.microsoft.com/windows/desktop/Controls/list-box-styles">LBS_OWNERDRAWVARIABLE</a> style, set this parameter to zero. 


## -remarks



For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/lb-getitemheight">LB_GETITEMHEIGHT</a>.
	



