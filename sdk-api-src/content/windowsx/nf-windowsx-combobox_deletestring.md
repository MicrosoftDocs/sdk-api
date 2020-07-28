---
UID: NF:windowsx.ComboBox_DeleteString
title: ComboBox_DeleteString macro (windowsx.h)
description: Deletes the item at the specified location in a list in a combo box. You can use this macro or send the CB_DELETESTRING message explicitly.
helpviewer_keywords: ["ComboBox_DeleteString","ComboBox_DeleteString macro [Windows Controls]","_win32_ComboBox_DeleteString","_win32_ComboBox_DeleteString_cpp","controls.ComboBox_DeleteString","controls._win32_ComboBox_DeleteString","windowsx/ComboBox_DeleteString"]
old-location: controls\ComboBox_DeleteString.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_deletestring.htm
ms.date: 12/05/2018
ms.keywords: ComboBox_DeleteString, ComboBox_DeleteString macro [Windows Controls], _win32_ComboBox_DeleteString, _win32_ComboBox_DeleteString_cpp, controls.ComboBox_DeleteString, controls._win32_ComboBox_DeleteString, windowsx/ComboBox_DeleteString
f1_keywords:
- windowsx/ComboBox_DeleteString
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
- ComboBox_DeleteString
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ComboBox_DeleteString macro


## -description


Deletes the item at the specified location in a list in a combo box. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/cb-deletestring">CB_DELETESTRING</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item to delete.


## -remarks



For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cb-deletestring">CB_DELETESTRING</a>




