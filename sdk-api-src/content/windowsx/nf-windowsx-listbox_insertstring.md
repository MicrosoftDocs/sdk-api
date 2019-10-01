---
UID: NF:windowsx.ListBox_InsertString
title: ListBox_InsertString macro (windowsx.h)
author: windows-sdk-content
description: Adds a string to a list box at the specified location. You can use this macro or send the LB_INSERTSTRING message explicitly.
old-location: controls\ListBox_InsertString.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_insertstring.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListBox_InsertString, ListBox_InsertString macro [Windows Controls], _win32_ListBox_InsertString, _win32_ListBox_InsertString_cpp, controls.ListBox_InsertString, controls._win32_ListBox_InsertString, windowsx/ListBox_InsertString
ms.topic: macro
f1_keywords: 
 - "windowsx/ListBox_InsertString"
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
 - ListBox_InsertString
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListBox_InsertString macro


## -description


Adds a string to a list box at the specified location. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lb-insertstring">LB_INSERTSTRING</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index at which to insert the string, or –1 to add it to the end of the list. 


### -param lpsz

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The string to add.


## -remarks



For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/lb-insertstring">LB_INSERTSTRING</a>.
	



