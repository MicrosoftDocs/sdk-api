---
UID: NF:commctrl.ListView_GetItemText
title: ListView_GetItemText macro (commctrl.h)
description: Gets the text of a list-view item or subitem. You can use this macro or send the LVM_GETITEMTEXT message explicitly.
helpviewer_keywords: ["ListView_GetItemText","ListView_GetItemText macro [Windows Controls]","_win32_ListView_GetItemText","_win32_ListView_GetItemText_cpp","commctrl/ListView_GetItemText","controls.ListView_GetItemText","controls._win32_ListView_GetItemText"]
old-location: controls\ListView_GetItemText.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getitemtext.htm
ms.date: 12/05/2018
ms.keywords: ListView_GetItemText, ListView_GetItemText macro [Windows Controls], _win32_ListView_GetItemText, _win32_ListView_GetItemText_cpp, commctrl/ListView_GetItemText, controls.ListView_GetItemText, controls._win32_ListView_GetItemText
f1_keywords:
- commctrl/ListView_GetItemText
dev_langs:
- c++
req.header: commctrl.h
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
- Commctrl.h
api_name:
- ListView_GetItemText
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

## -description

Gets the text of a list-view item or subitem. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-getitemtext">LVM_GETITEMTEXT</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 

### -param i

Type: <b>int</b>

The index of the list-view item. 

### -param iSubItem_

Type: <b>int</b>

The index of the subitem. To retrieve the item text, set 
					<i>iSubItem</i> to zero. 

### -param pszText_

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPTSTR</a></b>

A pointer to a buffer that receives the item or subitem text. 

### -param cchTextMax_

Type: <b>int</b>

The number of characters in the 
					<i>pszText</i> buffer.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a>
