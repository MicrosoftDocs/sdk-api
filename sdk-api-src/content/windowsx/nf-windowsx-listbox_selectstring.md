---
UID: NF:windowsx.ListBox_SelectString
title: ListBox_SelectString macro
author: windows-sdk-content
description: Searches a list box for an item that begins with the characters in a specified string. If a matching item is found, the item is selected. You can use this macro or send the LB_SELECTSTRING message explicitly.
old-location: controls\ListBox_SelectString.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_selectstring.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ListBox_SelectString, ListBox_SelectString macro [Windows Controls], _win32_ListBox_SelectString, _win32_ListBox_SelectString_cpp, controls.ListBox_SelectString, controls._win32_ListBox_SelectString, windowsx/ListBox_SelectString
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
 - ListBox_SelectString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListBox_SelectString macro


## -description


Searches a list box for an item that begins with the characters in a specified string. If a matching item is found, the item is selected. You can use this macro or send the <a href="https://msdn.microsoft.com/fd443ade-665d-439a-8951-3d9fed50695b">LB_SELECTSTRING</a> message explicitly.


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



For more information, see <a href="https://msdn.microsoft.com/fd443ade-665d-439a-8951-3d9fed50695b">LB_SELECTSTRING</a>.
	



