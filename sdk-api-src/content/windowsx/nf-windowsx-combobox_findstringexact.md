---
UID: NF:windowsx.ComboBox_FindStringExact
title: ComboBox_FindStringExact macro
author: windows-sdk-content
description: Finds the first string in a combo box list that exactly matches the specified string, except that the search is not case sensitive. You can use this macro or send the CB_FINDSTRINGEXACT message explicitly.
old-location: controls\ComboBox_FindStringExact.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_findstringexact.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ComboBox_FindStringExact, ComboBox_FindStringExact macro [Windows Controls], _win32_ComboBox_FindStringExact, _win32_ComboBox_FindStringExact_cpp, controls.ComboBox_FindStringExact, controls._win32_ComboBox_FindStringExact, windowsx/ComboBox_FindStringExact
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - ComboBox_FindStringExact
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# ComboBox_FindStringExact macro


## -description


Finds the first string in a combo box list that exactly matches the specified string, except that the search is not case sensitive. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb775837(v=VS.85).aspx">CB_FINDSTRINGEXACT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param indexStart

Type: <b>int</b>

The zero-based index of the item before the first item to be searched. When the search reaches the bottom of the list, it continues searching from the top of the list back to the item specified by the <i>indexStart</i> parameter. If <i>indexStart</i>  is –1, the entire list is searched from the beginning.


### -param lpszFind

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

The string to find.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb775837(v=VS.85).aspx">CB_FINDSTRINGEXACT</a>.
	



