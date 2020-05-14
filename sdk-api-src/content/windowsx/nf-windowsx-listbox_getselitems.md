---
UID: NF:windowsx.ListBox_GetSelItems
title: ListBox_GetSelItems macro (windowsx.h)
description: Gets the indexes of selected items in a multiple-selection list box. You can use this macro or send the LB_GETSELITEMS message explicitly.helpviewer_keywords: ["ListBox_GetSelItems","ListBox_GetSelItems macro [Windows Controls]","_win32_ListBox_GetSelItems","_win32_ListBox_GetSelItems_cpp","controls.ListBox_GetSelItems","controls._win32_ListBox_GetSelItems","windowsx/ListBox_GetSelItems"]
old-location: controls\ListBox_GetSelItems.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_getselitems.htm
ms.date: 12/05/2018
ms.keywords: ListBox_GetSelItems, ListBox_GetSelItems macro [Windows Controls], _win32_ListBox_GetSelItems, _win32_ListBox_GetSelItems_cpp, controls.ListBox_GetSelItems, controls._win32_ListBox_GetSelItems, windowsx/ListBox_GetSelItems
f1_keywords:
- windowsx/ListBox_GetSelItems
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
- ListBox_GetSelItems
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListBox_GetSelItems macro


## -description


Gets the indexes of selected items in a multiple-selection list box. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lb-getselitems">LB_GETSELITEMS</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param cItems

Type: <b>int</b>

The maximum number of selected items whose item numbers are to be placed in the buffer.


### -param lpItems

Type: <b>int*</b>

A pointer to a buffer large enough for the number of integers specified by <i>cItems</i>. 

