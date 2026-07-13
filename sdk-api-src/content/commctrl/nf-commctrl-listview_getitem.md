---
UID: NF:commctrl.ListView_GetItem
title: ListView_GetItem macro (commctrl.h)
description: Gets some or all of a list-view item's attributes. You can use this macro or send the LVM_GETITEM message explicitly.
helpviewer_keywords: ["ListView_GetItem","ListView_GetItem macro [Windows Controls]","_win32_ListView_GetItem","_win32_ListView_GetItem_cpp","commctrl/ListView_GetItem","controls.ListView_GetItem","controls._win32_ListView_GetItem"]
old-location: controls\ListView_GetItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getitem.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetItem, ListView_GetItem macro [Windows Controls], _win32_ListView_GetItem, _win32_ListView_GetItem_cpp, commctrl/ListView_GetItem, controls.ListView_GetItem, controls._win32_ListView_GetItem
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ListView_GetItem
 - commctrl/ListView_GetItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ListView_GetItem
---

# ListView_GetItem macro

## -syntax

```cpp
BOOL ListView_GetItem(
   HWND     hwnd,
   LPLVITEM pitem
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Gets some or all of a list-view item's attributes. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getitem">LVM_GETITEM</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param pitem

Type: <b>LPLVITEM</b>

A pointer to an <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure that specifies the information to retrieve and receives information about the list-view item.

## -remarks

When the <a href="/windows/desktop/Controls/lvm-getitem">LVM_GETITEM</a> message is sent, the 
				<b>iItem</b> and <b>iSubItem</b> members identify the item or subitem to retrieve information about and the <b>mask</b> member specifies which attributes to retrieve. For a list of possible values, see the description of the <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure.

If the LVIF_TEXT flag is set in the <b>mask</b> member of the <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure, the <b>pszText</b> member must point to a valid buffer and the <b>cchTextMax</b> member must be set to the number of characters in that buffer. Applications should not assume that the text will necessarily be placed in the specified buffer. The control may instead change the <b>pszText</b> member of the structure to point to the new text rather than place it in the buffer.

If the <b>mask</b> member specifies the LVIF_STATE value, the <b>stateMask</b> member must specify the item state bits to retrieve. On output, the <b>state</b> member contains the values of the specified state bits.
