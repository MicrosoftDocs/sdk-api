---
UID: NF:commctrl.ListView_GetItemRect
title: ListView_GetItemRect macro (commctrl.h)
description: Gets the bounding rectangle for all or part of an item in the current view. You can use this macro or send the LVM_GETITEMRECT message explicitly.
helpviewer_keywords: ["LVIR_BOUNDS","LVIR_ICON","LVIR_LABEL","LVIR_SELECTBOUNDS","ListView_GetItemRect","ListView_GetItemRect macro [Windows Controls]","_win32_ListView_GetItemRect","_win32_ListView_GetItemRect_cpp","commctrl/ListView_GetItemRect","controls.ListView_GetItemRect","controls._win32_ListView_GetItemRect"]
old-location: controls\ListView_GetItemRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getitemrect.htm
ms.date: 10/21/2024
ms.keywords: LVIR_BOUNDS, LVIR_ICON, LVIR_LABEL, LVIR_SELECTBOUNDS, ListView_GetItemRect, ListView_GetItemRect macro [Windows Controls], _win32_ListView_GetItemRect, _win32_ListView_GetItemRect_cpp, commctrl/ListView_GetItemRect, controls.ListView_GetItemRect, controls._win32_ListView_GetItemRect
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
 - ListView_GetItemRect
 - commctrl/ListView_GetItemRect
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
 - ListView_GetItemRect
---

# ListView_GetItemRect macro

## -syntax

```cpp
BOOL ListView_GetItemRect(
  [in]  HWND hwnd,
  [in]  int  i,
  [out] RECT *prc,
  [in]  int  code
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Gets the bounding rectangle for all or part of an item in the current view. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getitemrect">LVM_GETITEMRECT</a> message explicitly.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param i [in]

Type: <b>int</b>

The index of the list-view item.

### -param prc [out]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the bounding rectangle.

### -param code [in]

Type: <b>int</b>

The portion of the list-view item from which to retrieve the bounding rectangle. This parameter must be one of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVIR_BOUNDS"></a><a id="lvir_bounds"></a><dl>
<dt><b>LVIR_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
Returns the bounding rectangle of the entire item, including the icon and label.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIR_ICON"></a><a id="lvir_icon"></a><dl>
<dt><b>LVIR_ICON</b></dt>
</dl>
</td>
<td width="60%">
Returns the bounding rectangle of the icon or small icon.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIR_LABEL"></a><a id="lvir_label"></a><dl>
<dt><b>LVIR_LABEL</b></dt>
</dl>
</td>
<td width="60%">
Returns the bounding rectangle of the item text.

</td>
</tr>
<tr>
<td width="40%"><a id="LVIR_SELECTBOUNDS"></a><a id="lvir_selectbounds"></a><dl>
<dt><b>LVIR_SELECTBOUNDS</b></dt>
</dl>
</td>
<td width="60%">
Returns the union of the LVIR_ICON and LVIR_LABEL rectangles, but excludes columns in report view.

</td>
</tr>
</table>
