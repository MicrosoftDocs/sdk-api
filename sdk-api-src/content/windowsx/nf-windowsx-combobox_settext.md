---
UID: NF:windowsx.ComboBox_SetText
title: ComboBox_SetText macro (windowsx.h)
description: Sets the text of a combo box.
helpviewer_keywords: ["ComboBox_SetText","ComboBox_SetText macro [Windows Controls]","_win32_ComboBox_SetText","_win32_ComboBox_SetText_cpp","controls.ComboBox_SetText","controls._win32_ComboBox_SetText","windowsx/ComboBox_SetText"]
old-location: controls\ComboBox_SetText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_settext.htm
ms.date: 12/05/2018
ms.keywords: ComboBox_SetText, ComboBox_SetText macro [Windows Controls], _win32_ComboBox_SetText, _win32_ComboBox_SetText_cpp, controls.ComboBox_SetText, controls._win32_ComboBox_SetText, windowsx/ComboBox_SetText
f1_keywords:
- windowsx/ComboBox_SetText
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
- ComboBox_SetText
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ComboBox_SetText macro


## -description


Sets the text of a combo box.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param lpsz

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

A pointer to a null-terminated string to be used as the control text.


## -remarks



The macro expands to a call to <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setwindowtexta">SetWindowText</a>.	



