---
UID: NF:windowsx.ListBox_SelectString
title: ListBox_SelectString macro (windowsx.h)
description: Searches a list box for an item that begins with the characters in a specified string. If a matching item is found, the item is selected. You can use this macro or send the LB_SELECTSTRING message explicitly.
helpviewer_keywords: ["ListBox_SelectString","ListBox_SelectString macro [Windows Controls]","_win32_ListBox_SelectString","_win32_ListBox_SelectString_cpp","controls.ListBox_SelectString","controls._win32_ListBox_SelectString","windowsx/ListBox_SelectString"]
old-location: controls\ListBox_SelectString.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_selectstring.htm
ms.date: 12/05/2018
ms.keywords: ListBox_SelectString, ListBox_SelectString macro [Windows Controls], _win32_ListBox_SelectString, _win32_ListBox_SelectString_cpp, controls.ListBox_SelectString, controls._win32_ListBox_SelectString, windowsx/ListBox_SelectString
f1_keywords:
- windowsx/ListBox_SelectString
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
- ListBox_SelectString
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListBox_SelectString macro


## -description


Searches a list box for an item that begins with the characters in a specified string. If a matching item is found, the item is selected. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lb-selectstring">LB_SELECTSTRING</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param indexStart

Type: <b>int</b>

The zero-based index of the item before the first item to be searched. When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the <i>indexStart</i> parameter. If <i>indexStart</i>  is –1, the entire list box is searched from the beginning.


### -param lpszFind

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

The string to find.


## -remarks



For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/lb-selectstring">LB_SELECTSTRING</a>.
	



