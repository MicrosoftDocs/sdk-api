---
UID: NF:windowsx.ListBox_GetSel
title: ListBox_GetSel macro (windowsx.h)
description: Gets the selection state of an item. You can use this macro or send the LB_GETSEL message explicitly.
helpviewer_keywords: ["ListBox_GetSel","ListBox_GetSel macro [Windows Controls]","_win32_ListBox_GetSel","_win32_ListBox_GetSel_cpp","controls.ListBox_GetSel","controls._win32_ListBox_GetSel","windowsx/ListBox_GetSel"]
old-location: controls\ListBox_GetSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_getsel.htm
ms.date: 12/05/2018
ms.keywords: ListBox_GetSel, ListBox_GetSel macro [Windows Controls], _win32_ListBox_GetSel, _win32_ListBox_GetSel_cpp, controls.ListBox_GetSel, controls._win32_ListBox_GetSel, windowsx/ListBox_GetSel
f1_keywords:
- windowsx/ListBox_GetSel
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
- ListBox_GetSel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListBox_GetSel macro


## -description


Gets the selection state of an item. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lb-getsel">LB_GETSEL</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the control.


### -param index

Type: <b>int</b>

The zero-based index of the item.


## -remarks



For more information, see <a href="https://docs.microsoft.com/windows/desktop/Controls/lb-getsel">LB_GETSEL</a>




