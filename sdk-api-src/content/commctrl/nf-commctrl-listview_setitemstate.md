---
UID: NF:commctrl.ListView_SetItemState
title: ListView_SetItemState macro (commctrl.h)
description: Changes the state of an item in a list-view control. You can use this macro or send the LVM_SETITEMSTATE message explicitly.
helpviewer_keywords: ["LVIS_CUT","LVIS_DROPHILITED","LVIS_FOCUSED","LVIS_SELECTED","ListView_SetItemState","ListView_SetItemState macro [Windows Controls]","_win32_ListView_SetItemState","_win32_ListView_SetItemState_cpp","commctrl/ListView_SetItemState","controls.ListView_SetItemState","controls._win32_ListView_SetItemState"]
old-location: controls\ListView_SetItemState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setitemstate.htm
ms.date: 10/21/2024
ms.keywords: LVIS_CUT, LVIS_DROPHILITED, LVIS_FOCUSED, LVIS_SELECTED, ListView_SetItemState, ListView_SetItemState macro [Windows Controls], _win32_ListView_SetItemState, _win32_ListView_SetItemState_cpp, commctrl/ListView_SetItemState, controls.ListView_SetItemState, controls._win32_ListView_SetItemState
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
 - ListView_SetItemState
 - commctrl/ListView_SetItemState
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
 - ListView_SetItemState
---

# ListView_SetItemState macro

## -syntax

```cpp
void ListView_SetItemState(
   HWND hwndLV,
   int  i,
   UINT data,
   UINT mask
);
```


## -description

Changes the state of an item in a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-setitemstate">LVM_SETITEMSTATE</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param i

Type: <b>int</b>

The index of the list-view item. If this parameter is -1, then the state change is applied to all items.

### -param data

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

New state bits for the item. The <i>mask</i> parameter indicates the valid bits of the <i>data</i> parameter. The macro ignores bits in the <i>data</i> parameter if the corresponding bit is not set in the <i>mask</i> parameter. The low-order byte contains a set of bit flags that indicate the item's state. This byte can be a combination of the following values:

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
The item is selected. The appearance of a selected item depends on whether it has the focus and also on the system colors used for selection. Items will only show as selected if the list-view control has focus or the <a href="/windows/desktop/Controls/list-view-window-styles">LVS_SHOWSELALWAYS</a> style is used.

</td>
</tr>
</table>

### -param mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Bits of the <i>data</i> parameter that you want to set or clear. You can use <b>ListView_SetItemState</b> both to set and to clear bits. To set an item's overlay image index, set the <a href="/windows/desktop/Controls/list-view-item-states">LVIS_OVERLAYMASK</a> bits. To set an item's state image index, set the <a href="/windows/desktop/Controls/list-view-item-states">LVIS_STATEIMAGEMASK</a> bits.

## -remarks

An item's state value includes a set of bit flags that indicate the item's state. The state value can also include image list indexes that indicate the item's state image and overlay image.

The <i>mask</i> parameter specifies the state bits you want to modify, and the <i>data</i> parameter specifies the new value for those bits. To set a bit in the item's internal state, set it in both the <i>mask</i> and <i>data</i> parameters. To clear a bit in the item's internal state, set it in the <i>mask</i> parameter and clear it in the <i>data</i> parameter. To leave a bit unchanged in the item's internal state, clear it in the <i>mask</i> parameter.

Bits 8 through 11 of the <i>data</i> parameter specify the one-based index of an overlay image in the control's image lists. Both the full-sized icon image list and the small icon image list can have overlay images. The overlay image is superimposed over the item's icon image. If these bits are zero, the item has no overlay image. To isolate these bits, use the <a href="/windows/desktop/Controls/list-view-item-states">LVIS_OVERLAYMASK</a> mask. To specify an overlay index, use the <a href="/windows/desktop/api/commctrl/nf-commctrl-indextooverlaymask">INDEXTOOVERLAYMASK</a> macro.

Bits 12 through 15 of the <i>data</i> parameter specify the one-based index of an image in the control's state image list. The state image is displayed next to an item's icon to indicate an application-defined state. If these bits are zero, the item has no state image. To isolate these bits, use the <a href="/windows/desktop/Controls/list-view-item-states">LVIS_STATEIMAGEMASK</a> mask. To specify a state image index, use the <a href="/windows/desktop/api/commctrl/nf-commctrl-indextostateimagemask">INDEXTOSTATEIMAGEMASK</a> macro.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-listview_getitemstate">ListView_GetItemState</a>
