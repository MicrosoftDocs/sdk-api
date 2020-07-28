---
UID: NF:windowsx.ComboBox_GetItemHeight
title: ComboBox_GetItemHeight macro (windowsx.h)
description: Retrieves the height of list items in a combo box. You can use this macro or send the CB_GETITEMHEIGHT message explicitly.
helpviewer_keywords: ["ComboBox_GetItemHeight","ComboBox_GetItemHeight macro [Windows Controls]","_win32_ComboBox_GetItemHeight","_win32_ComboBox_GetItemHeight_cpp","controls.ComboBox_GetItemHeight","controls._win32_ComboBox_GetItemHeight","windowsx/ComboBox_GetItemHeight"]
old-location: controls\ComboBox_GetItemHeight.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\comboboxes\comboboxreference\comboboxmacros\combobox_getitemheight.htm
ms.date: 12/05/2018
ms.keywords: ComboBox_GetItemHeight, ComboBox_GetItemHeight macro [Windows Controls], _win32_ComboBox_GetItemHeight, _win32_ComboBox_GetItemHeight_cpp, controls.ComboBox_GetItemHeight, controls._win32_ComboBox_GetItemHeight, windowsx/ComboBox_GetItemHeight
f1_keywords:
- windowsx/ComboBox_GetItemHeight
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
- ComboBox_GetItemHeight
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ComboBox_GetItemHeight macro


## -description


Retrieves the height of list items in a combo box. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/cb-getitemheight">CB_GETITEMHEIGHT</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


## -remarks



This macro passes zero as the <i>wParam</i> member of <a href="https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cb-getitemheight">CB_GETITEMHEIGHT</a>.
	



