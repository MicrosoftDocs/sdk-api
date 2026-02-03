---
UID: NF:commctrl.ListView_SetItemCountEx
title: ListView_SetItemCountEx macro (commctrl.h)
description: Sets the virtual number of items in a virtual list view. You can use this macro or send the LVM_SETITEMCOUNT message explicitly.
helpviewer_keywords: ["LVSICF_NOINVALIDATEALL","LVSICF_NOSCROLL","ListView_SetItemCountEx","ListView_SetItemCountEx macro [Windows Controls]","_win32_ListView_SetItemCountEx","_win32_ListView_SetItemCountEx_cpp","commctrl/ListView_SetItemCountEx","controls.ListView_SetItemCountEx","controls._win32_ListView_SetItemCountEx"]
old-location: controls\ListView_SetItemCountEx.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setitemcountex.htm
ms.date: 10/21/2024
ms.keywords: LVSICF_NOINVALIDATEALL, LVSICF_NOSCROLL, ListView_SetItemCountEx, ListView_SetItemCountEx macro [Windows Controls], _win32_ListView_SetItemCountEx, _win32_ListView_SetItemCountEx_cpp, commctrl/ListView_SetItemCountEx, controls.ListView_SetItemCountEx, controls._win32_ListView_SetItemCountEx
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
 - ListView_SetItemCountEx
 - commctrl/ListView_SetItemCountEx
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
 - ListView_SetItemCountEx
---

# ListView_SetItemCountEx macro

## -syntax

```cpp
LRESULT ListView_SetItemCountEx(
   HWND  hwndLV,
   int   cItems,
   DWORD dwFlags
);
```


## -description

Sets the virtual number of items in a <a href="/windows/desktop/Controls/list-view-controls-overview">virtual list view</a>. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-setitemcount">LVM_SETITEMCOUNT</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a virtual list-view control.

### -param cItems

Type: <b>int</b>

The number of items that the list-view control will contain.

### -param dwFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Values that specify the behavior of the list-view control after resetting the item count. This value can be a combination of the following: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVSICF_NOINVALIDATEALL"></a><a id="lvsicf_noinvalidateall"></a><dl>
<dt><b>LVSICF_NOINVALIDATEALL</b></dt>
</dl>
</td>
<td width="60%">
The list-view control will not repaint unless affected items are currently in view.

</td>
</tr>
<tr>
<td width="40%"><a id="LVSICF_NOSCROLL"></a><a id="lvsicf_noscroll"></a><dl>
<dt><b>LVSICF_NOSCROLL</b></dt>
</dl>
</td>
<td width="60%">
The list-view control will not change the scroll position when the item count changes.

</td>
</tr>
</table>

## -returns

Type: <b>LRESULT</b>

Returns nonzero if successful, or zero otherwise.

## -remarks

This macro is intended only for list-view controls that use the <a href="/windows/desktop/Controls/list-view-window-styles">LVS_OWNERDATA</a> and <a href="/windows/desktop/Controls/list-view-window-styles">LVS_REPORT</a> or <a href="/windows/desktop/Controls/list-view-window-styles">LVS_LIST</a> styles. 

If the list-view control was created with the <a href="/windows/desktop/Controls/list-view-window-styles">LVS_OWNERDATA</a> style, this macro sets the virtual number of items that the control contains. 

If the list-view control was created without the <a href="/windows/desktop/Controls/list-view-window-styles">LVS_OWNERDATA</a> style, the <a href="/windows/desktop/api/commctrl/nf-commctrl-listview_setitemcount">ListView_SetItemCount</a> macro should be used.
