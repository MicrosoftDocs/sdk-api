---
UID: NF:windowsx.ComboBox_FindString
title: ComboBox_FindString macro (windowsx.h)
description: Finds the first string in a combo box list that begins with the specified string. You can use this macro or send the CB_FINDSTRING message explicitly.
helpviewer_keywords: ["ComboBox_FindString","ComboBox_FindString macro [Windows Controls]","_win32_ComboBox_FindString","_win32_ComboBox_FindString_cpp","controls.ComboBox_FindString","controls._win32_ComboBox_FindString","windowsx/ComboBox_FindString"]
old-location: controls\ComboBox_FindString.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_findstring.htm
ms.date: 12/05/2018
ms.keywords: ComboBox_FindString, ComboBox_FindString macro [Windows Controls], _win32_ComboBox_FindString, _win32_ComboBox_FindString_cpp, controls.ComboBox_FindString, controls._win32_ComboBox_FindString, windowsx/ComboBox_FindString
f1_keywords:
- windowsx/ComboBox_FindString
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
- ComboBox_FindString
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ComboBox_FindString macro


## -description


Finds the first string in a combo box list that begins with the specified string. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/cb-findstring">CB_FINDSTRING</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param indexStart

Type: <b>int</b>

The zero-based index of the item before the first item to be searched. When the search reaches the bottom of the list, it continues searching from the top of the list back to the item specified by the <i>indexStart</i> parameter. If <i>indexStart</i>  is –1, the entire list is searched from the beginning.


### -param lpszFind

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

The string to find.


## -remarks



For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cb-findstring">CB_FINDSTRING</a>.
	



