---
UID: NF:windowsx.ComboBox_GetText
title: ComboBox_GetText macro (windowsx.h)
description: Retrieves the text from a combo box control.helpviewer_keywords: ["ComboBox_GetText","ComboBox_GetText macro [Windows Controls]","_win32_ComboBox_GetText","_win32_ComboBox_GetText_cpp","controls.ComboBox_GetText","controls._win32_ComboBox_GetText","windowsx/ComboBox_GetText"]
old-location: controls\ComboBox_GetText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\combobox_gettext.htm
ms.date: 12/05/2018
ms.keywords: ComboBox_GetText, ComboBox_GetText macro [Windows Controls], _win32_ComboBox_GetText, _win32_ComboBox_GetText_cpp, controls.ComboBox_GetText, controls._win32_ComboBox_GetText, windowsx/ComboBox_GetText
f1_keywords:
- windowsx/ComboBox_GetText
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
- ComboBox_GetText
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ComboBox_GetText macro


## -description


Retrieves the text from a combo box control.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param lpch

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

A pointer to the buffer that will receive the text.


### -param cchMax

Type: <b>int</b>

The maximum number of characters to copy to the buffer, including the NULL terminator.


## -remarks



The macro expands to a call to <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowtexta">GetWindowText</a>.
	



