---
UID: NF:commctrl.ListView_SetItem
title: ListView_SetItem macro (commctrl.h)
description: Sets some or all of a list-view item's attributes. You can also use ListView_SetItem to set the text of a subitem. You can use this macro or send the LVM_SETITEM message explicitly.
helpviewer_keywords: ["ListView_SetItem","ListView_SetItem macro [Windows Controls]","_win32_ListView_SetItem","_win32_ListView_SetItem_cpp","commctrl/ListView_SetItem","controls.ListView_SetItem","controls._win32_ListView_SetItem"]
old-location: controls\ListView_SetItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setitem.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetItem, ListView_SetItem macro [Windows Controls], _win32_ListView_SetItem, _win32_ListView_SetItem_cpp, commctrl/ListView_SetItem, controls.ListView_SetItem, controls._win32_ListView_SetItem
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
 - ListView_SetItem
 - commctrl/ListView_SetItem
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
 - ListView_SetItem
---

# ListView_SetItem macro

## -syntax

```cpp
BOOL ListView_SetItem(
         HWND     hwnd,
   const LPLVITEM pitem
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Sets some or all of a list-view item's attributes. You can also use <b>ListView_SetItem</b> to set the text of a subitem. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-setitem">LVM_SETITEM</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param pitem

Type: <b>const LPLVITEM</b>

A pointer to an <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure that contains the new item attributes. The <b>iItem</b> and 
<b>iSubItem</b> members identify the item or subitem, and the 
					<b>mask</b> member specifies which attributes to set. If the <b>mask</b> member specifies the LVIF_TEXT value, the <b>pszText</b> member is the address of a null-terminated string and the <b>cchTextMax</b> member is ignored. If the <b>mask</b> member specifies the LVIF_STATE value, the <b>stateMask</b> member specifies which item states to change, and the <b>state</b> member contains the values for those states.

## -remarks

To set the attributes of a list-view item, set the 
				<b>iItem</b> member of the <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure to the index of the item, and set the 
<b>iSubItem</b> member to zero. For an item, you can use the 
<b>state</b>, <b>pszText</b>, 
<b>iImage</b>, and <b>lParam</b> members of the <b>LVITEM</b> structure to modify these item parameters. 

To set the text of a subitem, set the <b>iItem</b> and <b>iSubItem</b> members to indicate the specific subitem, and use the <b>pszText</b> member to specify the text. Alternatively, you can use the <a href="/windows/desktop/api/commctrl/nf-commctrl-listview_setitemtext">ListView_SetItemText</a> macro to set the text of a subitem. You cannot set the <b>state</b> or <b>lParam</b> members for subitems because subitems do not have these attributes. In version 4.70 and later, you can set the <b>iImage</b> member for subitems. The subitem image will be displayed if the list-view control has the <a href="/windows/desktop/Controls/extended-list-view-styles">LVS_EX_SUBITEMIMAGES</a> extended style. Previous versions will ignore the subitem image.
