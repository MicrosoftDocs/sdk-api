---
UID: NF:windowsx.ListBox_FindStringExact
title: ListBox_FindStringExact macro (windowsx.h)
description: Finds the first list box string that exactly matches the specified string, except that the search is not case sensitive. You can use this macro or send the LB_FINDSTRINGEXACT message explicitly.
helpviewer_keywords: ["ListBox_FindStringExact","ListBox_FindStringExact macro [Windows Controls]","_win32_ListBox_FindStringExact","_win32_ListBox_FindStringExact_cpp","controls.ListBox_FindStringExact","controls._win32_ListBox_FindStringExact","windowsx/ListBox_FindStringExact"]
old-location: controls\ListBox_FindStringExact.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_findstringexact.htm
ms.date: 12/05/2018
ms.keywords: ListBox_FindStringExact, ListBox_FindStringExact macro [Windows Controls], _win32_ListBox_FindStringExact, _win32_ListBox_FindStringExact_cpp, controls.ListBox_FindStringExact, controls._win32_ListBox_FindStringExact, windowsx/ListBox_FindStringExact
f1_keywords:
- windowsx/ListBox_FindStringExact
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
- ListBox_FindStringExact
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListBox_FindStringExact macro


## -description


Finds the first list box string that exactly matches the specified string, except that the search is not case sensitive. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lb-findstringexact">LB_FINDSTRINGEXACT</a> message explicitly.


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



For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/lb-findstringexact">LB_FINDSTRINGEXACT</a>.
	




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/windowsx/nf-windowsx-listbox_findstring">ListBox_FindString</a>
 

 

