---
UID: NF:commctrl.ListView_GetItemState
title: ListView_GetItemState macro (commctrl.h)
description: Gets the state of a list-view item. You can use this macro or send the LVM_GETITEMSTATE message explicitly.
helpviewer_keywords: ["LVIS_CUT","LVIS_DROPHILITED","LVIS_FOCUSED","LVIS_OVERLAYMASK","LVIS_SELECTED","LVIS_STATEIMAGEMASK","ListView_GetItemState","ListView_GetItemState macro [Windows Controls]","_win32_ListView_GetItemState","_win32_ListView_GetItemState_cpp","commctrl/ListView_GetItemState","controls.ListView_GetItemState","controls._win32_ListView_GetItemState"]
old-location: controls\ListView_GetItemState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getitemstate.htm
ms.date: 10/21/2024
ms.keywords: LVIS_CUT, LVIS_DROPHILITED, LVIS_FOCUSED, LVIS_OVERLAYMASK, LVIS_SELECTED, LVIS_STATEIMAGEMASK, ListView_GetItemState, ListView_GetItemState macro [Windows Controls], _win32_ListView_GetItemState, _win32_ListView_GetItemState_cpp, commctrl/ListView_GetItemState, controls.ListView_GetItemState, controls._win32_ListView_GetItemState
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
 - ListView_GetItemState
 - commctrl/ListView_GetItemState
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
 - ListView_GetItemState
---

# ListView_GetItemState macro

## -syntax

```cpp
UINT ListView_GetItemState(
   HWND hwndLV,
   int  i,
   UINT mask
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns the current state for the specified item. The only valid bits in the return value are those that correspond to the bits set in the <i>mask</i> parameter.


## -description

Gets the state of a list-view item. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getitemstate">LVM_GETITEMSTATE</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param i

Type: <b>int</b>

The index of the list-view item.

### -param mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The state information to retrieve. This parameter can be a combination of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVIS_CUT"></a><a id="lvis_cut"></a><dl>
<dt><b>LVIS_CUT</b></dt>
</dl>
</td>
<td width="60%">
The item is marked for a cut-and-paste operation.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIS_DROPHILITED"></a><a id="lvis_drophilited"></a><dl>
<dt><b>LVIS_DROPHILITED</b></dt>
</dl>
</td>
<td width="60%">
The item is highlighted as a drag-and-drop target.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIS_FOCUSED"></a><a id="lvis_focused"></a><dl>
<dt><b>LVIS_FOCUSED</b></dt>
</dl>
</td>
<td width="60%">
The item has the focus, so it is surrounded by a standard focus rectangle. Although more than one item may be selected, only one item can have the focus.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIS_SELECTED"></a><a id="lvis_selected"></a><dl>
<dt><b>LVIS_SELECTED</b></dt>
</dl>
</td>
<td width="60%">
The item is selected. The appearance of a selected item depends on whether it has the focus and also on the system colors used for selection.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIS_OVERLAYMASK"></a><a id="lvis_overlaymask"></a><dl>
<dt><b>LVIS_OVERLAYMASK</b></dt>
</dl>
</td>
<td width="60%">
Use this mask to retrieve the item's overlay image index.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIS_STATEIMAGEMASK"></a><a id="lvis_stateimagemask"></a><dl>
<dt><b>LVIS_STATEIMAGEMASK</b></dt>
</dl>
</td>
<td width="60%">
Use this mask to retrieve the item's state image index.

</td>
</tr>
</table>

## -remarks

An item's state information includes a set of bit flags as well as image list indexes that indicate the item's state image and overlay image.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-listview_setitemstate">ListView_SetItemState</a>
