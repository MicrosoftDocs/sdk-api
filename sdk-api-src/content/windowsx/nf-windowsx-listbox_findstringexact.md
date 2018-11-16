---
UID: NF:windowsx.ListBox_FindStringExact
title: ListBox_FindStringExact macro
author: windows-sdk-content
description: Finds the first list box string that exactly matches the specified string, except that the search is not case sensitive. You can use this macro or send the LB_FINDSTRINGEXACT message explicitly.
old-location: controls\ListBox_FindStringExact.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_findstringexact.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ListBox_FindStringExact, ListBox_FindStringExact macro [Windows Controls], _win32_ListBox_FindStringExact, _win32_ListBox_FindStringExact_cpp, controls.ListBox_FindStringExact, controls._win32_ListBox_FindStringExact, windowsx/ListBox_FindStringExact
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
 - ListBox_FindStringExact
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- windowsx.h
: 
- ListBox_FindStringExact
: 
---

# ListBox_FindStringExact macro


## -description


Finds the first list box string that exactly matches the specified string, except that the search is not case sensitive. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775189(v=VS.85).aspx">LB_FINDSTRINGEXACT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param indexStart

Type: <b>int</b>

The zero-based index of the item before the first item to be searched. When the search reaches the bottom of the list box, it continues searching from the top of the list box back to the item specified by the <i>indexStart</i> parameter. If <i>indexStart</i>  is –1, the entire list box is searched from the beginning.


### -param lpszFind

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

The string to find.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb775189(v=VS.85).aspx">LB_FINDSTRINGEXACT</a>.
	




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb856431(v=VS.85).aspx">ListBox_FindString</a>
 

 

