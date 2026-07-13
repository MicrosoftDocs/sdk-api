---
UID: NF:commctrl.ListView_GetSubItemRect
title: ListView_GetSubItemRect macro (commctrl.h)
description: Gets information about the rectangle that surrounds a subitem in a list-view control.
helpviewer_keywords: ["LVIR_BOUNDS","LVIR_ICON","LVIR_LABEL","ListView_GetSubItemRect","ListView_GetSubItemRect macro [Windows Controls]","_win32_ListView_GetSubItemRect","_win32_ListView_GetSubItemRect_cpp","commctrl/ListView_GetSubItemRect","controls.ListView_GetSubItemRect","controls._win32_ListView_GetSubItemRect"]
old-location: controls\ListView_GetSubItemRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getsubitemrect.htm
ms.date: 10/21/2024
ms.keywords: LVIR_BOUNDS, LVIR_ICON, LVIR_LABEL, ListView_GetSubItemRect, ListView_GetSubItemRect macro [Windows Controls], _win32_ListView_GetSubItemRect, _win32_ListView_GetSubItemRect_cpp, commctrl/ListView_GetSubItemRect, controls.ListView_GetSubItemRect, controls._win32_ListView_GetSubItemRect
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
 - ListView_GetSubItemRect
 - commctrl/ListView_GetSubItemRect
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
 - ListView_GetSubItemRect
---

# ListView_GetSubItemRect macro

## -syntax

```cpp
BOOL ListView_GetSubItemRect(
   HWND   hwnd,
   int    iItem,
   int    iSubItem,
   int    code,
   LPRECT prc
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns nonzero if successful, or zero otherwise.


## -description

Gets information about the rectangle that surrounds a subitem in a list-view control. You can use this macro (recommended) or send the <a href="/windows/desktop/Controls/lvm-getsubitemrect">LVM_GETSUBITEMRECT</a> message explicitly. This macro is intended to be used only on list-view controls that use the <a href="/windows/desktop/Controls/list-view-window-styles">LVS_REPORT</a> style.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a list-view control.

### -param iItem

Type: <b>int</b>

The index of the subitem's parent item.

### -param iSubItem

Type: <b>int</b>

The one-based index of the subitem.

### -param code

Type: <b>int</b>

A portion of the list-view subitem for which to retrieve the bounding rectangle information. This value can be one of the following: 

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
Returns the bounding rectangle of the entire item, including the icon and label. This is identical to LVIR_BOUNDS.

</td>
</tr>
</table>

### -param prc

Type: <b>LPRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the subitem bounding rectangle information.
