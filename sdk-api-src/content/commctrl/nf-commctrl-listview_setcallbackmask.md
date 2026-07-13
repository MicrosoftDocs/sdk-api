---
UID: NF:commctrl.ListView_SetCallbackMask
title: ListView_SetCallbackMask macro (commctrl.h)
description: Changes the callback mask for a list-view control. You can use this macro or send the LVM_SETCALLBACKMASK message explicitly.
helpviewer_keywords: ["LVIS_CUT","LVIS_DROPHILITED","LVIS_FOCUSED","LVIS_OVERLAYMASK","LVIS_SELECTED","LVIS_STATEIMAGEMASK","ListView_SetCallbackMask","ListView_SetCallbackMask macro [Windows Controls]","_win32_ListView_SetCallbackMask","_win32_ListView_SetCallbackMask_cpp","commctrl/ListView_SetCallbackMask","controls.ListView_SetCallbackMask","controls._win32_ListView_SetCallbackMask"]
old-location: controls\ListView_SetCallbackMask.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setcallbackmask.htm
ms.date: 10/21/2024
ms.keywords: LVIS_CUT, LVIS_DROPHILITED, LVIS_FOCUSED, LVIS_OVERLAYMASK, LVIS_SELECTED, LVIS_STATEIMAGEMASK, ListView_SetCallbackMask, ListView_SetCallbackMask macro [Windows Controls], _win32_ListView_SetCallbackMask, _win32_ListView_SetCallbackMask_cpp, commctrl/ListView_SetCallbackMask, controls.ListView_SetCallbackMask, controls._win32_ListView_SetCallbackMask
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
 - ListView_SetCallbackMask
 - commctrl/ListView_SetCallbackMask
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
 - ListView_SetCallbackMask
---

# ListView_SetCallbackMask macro

## -syntax

```cpp
BOOL ListView_SetCallbackMask(
   HWND hwnd,
   UINT mask
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Changes the callback mask for a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-setcallbackmask">LVM_SETCALLBACKMASK</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The value of the callback mask. The bits of the mask indicate the item states or images for which the application stores the current state data. This value can be any combination of the following constants: 

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
The item has the focus.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIS_SELECTED"></a><a id="lvis_selected"></a><dl>
<dt><b>LVIS_SELECTED</b></dt>
</dl>
</td>
<td width="60%">
The item is selected. 

</td>
</tr>
<tr>
<td width="40%"><a id="LVIS_OVERLAYMASK"></a><a id="lvis_overlaymask"></a><dl>
<dt><b>LVIS_OVERLAYMASK</b></dt>
</dl>
</td>
<td width="60%">
The application stores the image list index of the current overlay image for each item.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIS_STATEIMAGEMASK"></a><a id="lvis_stateimagemask"></a><dl>
<dt><b>LVIS_STATEIMAGEMASK</b></dt>
</dl>
</td>
<td width="60%">
The application stores the image list index of the current state image for each item. 

</td>
</tr>
</table>

## -remarks

The <i>callback mask</i> of a list-view control is a set of bit flags that specify the item states for which the application, rather than the control, stores the current data. The callback mask applies to all of the control's items, unlike the callback item designation, which applies to a specific item. The callback mask is zero by default, meaning that the list-view control stores all item state information. After creating a list-view control and initializing its items, you can use the <b>ListView_SetCallbackMask</b> macro or <a href="/windows/desktop/Controls/lvm-setcallbackmask">LVM_SETCALLBACKMASK</a> message to change the callback mask. To retrieve the current callback mask, send the <a href="/windows/desktop/Controls/lvm-getcallbackmask">LVM_GETCALLBACKMASK</a> message. 

For more information about overlay images and state images, see <a href="/windows/desktop/Controls/list-view-controls-overview">List-View Image Lists</a>. 

For more information on list-view callbacks, see <a href="/windows/desktop/Controls/list-view-controls-overview">Callback Items and the Callback Mask</a>

## -see-also

<a href="/windows/desktop/Controls/lvn-getdispinfo">LVN_GETDISPINFO</a>
