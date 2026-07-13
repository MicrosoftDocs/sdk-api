---
UID: NF:commctrl.ListView_GetNextItemIndex
title: ListView_GetNextItemIndex macro (commctrl.h)
description: Gets the index of the item in a particular list-view control that has the specified properties and relationship to another specific item. Use this macro or send the LVM_GETNEXTITEMINDEX message explicitly.
helpviewer_keywords: ["ListView_GetNextItemIndex","ListView_GetNextItemIndex macro [Windows Controls]","_shell_ListView_GetNextItemIndex","_shell_ListView_GetNextItemIndex_cpp","commctrl/ListView_GetNextItemIndex","controls.ListView_GetNextItemIndex","controls._shell_ListView_GetNextItemIndex"]
old-location: controls\ListView_GetNextItemIndex.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getnextitemindex.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetNextItemIndex, ListView_GetNextItemIndex macro [Windows Controls], _shell_ListView_GetNextItemIndex, _shell_ListView_GetNextItemIndex_cpp, commctrl/ListView_GetNextItemIndex, controls.ListView_GetNextItemIndex, controls._shell_ListView_GetNextItemIndex
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - ListView_GetNextItemIndex
 - commctrl/ListView_GetNextItemIndex
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
 - ListView_GetNextItemIndex
---

# ListView_GetNextItemIndex macro

## -syntax

```cpp
BOOL ListView_GetNextItemIndex(
  [in]      HWND        hwnd,
  [in, out] LVITEMINDEX *plvii,
            LPARAM      flags
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Gets the index of the item in a particular list-view control that has the specified properties and relationship to another specific item. Use this macro or send the <a href="/windows/desktop/controls/lvm-getnextitemindex">LVM_GETNEXTITEMINDEX</a> message explicitly.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param plvii [in, out]

Type: <b><a href="/windows/desktop/api/commctrl/ns-commctrl-lvitemindex">LVITEMINDEX</a>*</b>

A pointer to the <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitemindex">LVITEMINDEX</a> structure with which the item begins the search, or -1 to find the first item that matches the specified flags. The calling process is responsible for allocating this structure and setting its members.

### -param flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPARAM</a></b>

The relationship to the item specified in parameter 
					<i>plvii</i>. This can be one or a combination of the following values: 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>Searches by index.</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVNI_ALL</dt>
</dl>
</td>
<td width="60%">
Searches for a subsequent item by index, the default value.



</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>Searches by physical relationship to the index of the item where the search is to begin.</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVNI_ABOVE</dt>
</dl>
</td>
<td width="60%">
Searches for an item that is above the specified item.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVNI_BELOW</dt>
</dl>
</td>
<td width="60%">
Searches for an item that is below the specified item.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVNI_TOLEFT</dt>
</dl>
</td>
<td width="60%">
Searches for an item to the left of the specified item.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVNI_PREVIOUS</dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista and later:</b> Searches for the item that is previous to the specified item. The LVNI_PREVIOUS flag is not directional (LVNI_ABOVE will find the item positioned above, while LVNI_PREVIOUS will find the item ordered before.)  The LVNI_PREVIOUS flag essentially reverses the logic of the search performed via the LVM_GETNEXTITEM or LVM_GETNEXTITEMINDEX messages.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVNI_TORIGHT</dt>
</dl>
</td>
<td width="60%">
Searches for an item to the right of the specified item.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVNI_DIRECTIONMASK</dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista and later:</b> A directional flag mask with value as follows: LVNI_ABOVE | LVNI_BELOW | LVNI_TOLEFT | LVNI_TORIGHT.



</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>The state of the item to find can be specified with one or a combination of the following values:</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVNI_CUT</dt>
</dl>
</td>
<td width="60%">
The item has the <a href="/windows/desktop/Controls/list-view-item-states">LVIS_CUT</a> state flag set.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVNI_DROPHILITED</dt>
</dl>
</td>
<td width="60%">
The item has the <a href="/windows/desktop/Controls/list-view-item-states">LVIS_DROPHILITED</a> state flag set

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVNI_FOCUSED</dt>
</dl>
</td>
<td width="60%">
The item has the <a href="/windows/desktop/Controls/list-view-item-states">LVIS_FOCUSED</a> state flag set.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVNI_SELECTED</dt>
</dl>
</td>
<td width="60%">
The item has the <a href="/windows/desktop/Controls/list-view-item-states">LVIS_SELECTED</a> state flag set.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVNI_STATEMASK</dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista and later:</b> A state flag mask with value as follows: LVNI_FOCUSED | LVNI_SELECTED | LVNI_CUT | LVNI_DROPHILITED.



</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>Searches by appearance of items or by group.</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVNI_VISIBLEORDER</dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista and later:</b> Search the visible order.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVNI_VISIBLEONLY</dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista and later:</b> Search the visible items.

</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>LVNI_SAMEGROUPONLY</dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista and later:</b> Search the current group.



</td>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>If an item does not have all of the specified state flags set, the search continues with the next item.</dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -remarks

Note that the following flags, for use only with Windows Vista, are mutually exclusive of any other flags in use: LVNI_PREVIOUS, LVNI_VISIBLEONLY, LVNI_SAMEGROUPONLY, LVNI_VISIBLEORDER, LVNI_DIRECTIONMASK, and LVNI_STATEMASK.

## -see-also

<a href="/windows/desktop/Controls/lvm-getnextitem">LVM_GETNEXTITEM</a>
