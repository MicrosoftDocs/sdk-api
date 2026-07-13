---
UID: NF:commctrl.ListView_Arrange
title: ListView_Arrange macro (commctrl.h)
description: Arranges items in icon view. You can use this macro or send the LVM_ARRANGE message explicitly.
helpviewer_keywords: ["LVA_ALIGNLEFT","LVA_ALIGNTOP","LVA_DEFAULT","LVA_SNAPTOGRID","ListView_Arrange","ListView_Arrange macro [Windows Controls]","_win32_ListView_Arrange","_win32_ListView_Arrange_cpp","commctrl/ListView_Arrange","controls.ListView_Arrange","controls._win32_ListView_Arrange"]
old-location: controls\ListView_Arrange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_arrange.htm
ms.date: 10/21/2024
ms.keywords: LVA_ALIGNLEFT, LVA_ALIGNTOP, LVA_DEFAULT, LVA_SNAPTOGRID, ListView_Arrange, ListView_Arrange macro [Windows Controls], _win32_ListView_Arrange, _win32_ListView_Arrange_cpp, commctrl/ListView_Arrange, controls.ListView_Arrange, controls._win32_ListView_Arrange
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
 - ListView_Arrange
 - commctrl/ListView_Arrange
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
 - ListView_Arrange
---

# ListView_Arrange macro

## -syntax

```cpp
BOOL ListView_Arrange(
   HWND hwndLV,
   UINT code
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>.


## -description

Arranges items in icon view. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-arrange">LVM_ARRANGE</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param code

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

One of the following values that specifies alignment:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVA_ALIGNLEFT"></a><a id="lva_alignleft"></a><dl>
<dt><b>LVA_ALIGNLEFT</b></dt>
</dl>
</td>
<td width="60%">
Not implemented. Apply the <a href="/windows/desktop/Controls/list-view-window-styles">LVS_ALIGNLEFT</a> style instead.

</td>
</tr>
<tr>
<td width="40%"><a id="LVA_ALIGNTOP"></a><a id="lva_aligntop"></a><dl>
<dt><b>LVA_ALIGNTOP</b></dt>
</dl>
</td>
<td width="60%">
Not implemented. Apply the <a href="/windows/desktop/Controls/list-view-window-styles">LVS_ALIGNTOP</a> style instead.

</td>
</tr>
<tr>
<td width="40%"><a id="LVA_DEFAULT"></a><a id="lva_default"></a><dl>
<dt><b>LVA_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Aligns items according to the list-view control's current alignment styles (the default value).

</td>
</tr>
<tr>
<td width="40%"><a id="LVA_SNAPTOGRID"></a><a id="lva_snaptogrid"></a><dl>
<dt><b>LVA_SNAPTOGRID</b></dt>
</dl>
</td>
<td width="60%">
Snaps all icons to the nearest grid position.

</td>
</tr>
</table>
