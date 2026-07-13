---
UID: NF:commctrl.ListView_InsertItem
title: ListView_InsertItem macro (commctrl.h)
description: Inserts a new item in a list-view control. You can use this macro or send the LVM_INSERTITEM message explicitly.
helpviewer_keywords: ["ListView_InsertItem","ListView_InsertItem macro [Windows Controls]","_win32_ListView_InsertItem","_win32_ListView_InsertItem_cpp","commctrl/ListView_InsertItem","controls.ListView_InsertItem","controls._win32_ListView_InsertItem"]
old-location: controls\ListView_InsertItem.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_insertitem.htm
ms.date: 10/21/2024
ms.keywords: ListView_InsertItem, ListView_InsertItem macro [Windows Controls], _win32_ListView_InsertItem, _win32_ListView_InsertItem_cpp, commctrl/ListView_InsertItem, controls.ListView_InsertItem, controls._win32_ListView_InsertItem
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
 - ListView_InsertItem
 - commctrl/ListView_InsertItem
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
 - ListView_InsertItem
---

# ListView_InsertItem macro

## -syntax

```cpp
int ListView_InsertItem(
         HWND     hwnd,
   const LPLVITEM pitem
);
```

## -returns

Type: **int**

Returns the index of the new item if successful, or -1 otherwise.


## -description

Inserts a new item in a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-insertitem">LVM_INSERTITEM</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param pitem

Type: <b>const LPLVITEM</b>

A pointer to an <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure that specifies the attributes of the list-view item. Use the <b>iItem</b> member to specify the zero-based index at which the new item should be inserted. If this value is greater than the number of items currently contained by the listview control, the new item will be appended to the end of the list and assigned the correct index. Examine the macro's return value to determine the actual index assigned to the item.

## -remarks

You cannot use <b>ListView_InsertItem</b> or <a href="/windows/desktop/Controls/lvm-insertitem">LVM_INSERTITEM</a> to insert subitems. The <b>iSubItem</b> member of the <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure must be zero. See <a href="/windows/desktop/Controls/lvm-setitem">LVM_SETITEM</a> for information on setting subitems.

If a list-view control has the <a href="/windows/desktop/Controls/extended-list-view-styles">LVS_EX_CHECKBOXES</a> style set, any value placed in bits 12 through 15 of the <b>state</b> member of the <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure will be ignored. When an item is added with this style set, it will always be set to the unchecked state.

If a list-view control has either the <a href="/windows/desktop/Controls/list-view-window-styles">LVS_SORTASCENDING</a> or <a href="/windows/desktop/Controls/list-view-window-styles">LVS_SORTDESCENDING</a> window style, an <a href="/windows/desktop/Controls/lvm-insertitem">LVM_INSERTITEM</a> message will fail if you try to insert an item that has LPSTR_TEXTCALLBACK as the <b>pszText</b> member of its <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a> structure. 

The <b>ListView_InsertItem</b> macro will insert the new item in the proper position in the sort order if the following conditions hold: 

<ul>
<li>You are using one of the LVS_SORTXXX styles. </li>
<li>You are not using the LVS_OWNERDRAW style. </li>
<li>The 
						<b>pszText</b> member of the structure pointed to by <i>pitem</i> is not set to LPSTR_TEXTCALLBACK. </li>
</ul>
