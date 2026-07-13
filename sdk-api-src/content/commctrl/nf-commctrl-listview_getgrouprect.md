---
UID: NF:commctrl.ListView_GetGroupRect
title: ListView_GetGroupRect macro (commctrl.h)
description: Gets the rectangle for a specified group. Use this macro or send the LVM_GETGROUPRECT message explicitly.
helpviewer_keywords: ["LVGGR_GROUP","LVGGR_HEADER","LVGGR_LABEL","LVGGR_SUBSETLINK","ListView_GetGroupRect","ListView_GetGroupRect macro [Windows Controls]","_shell_ListView_GetGroupRect","_shell_ListView_GetGroupRect_cpp","commctrl/ListView_GetGroupRect","controls.ListView_GetGroupRect","controls._shell_ListView_GetGroupRect"]
old-location: controls\ListView_GetGroupRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getgrouprect.htm
ms.date: 10/21/2024
ms.keywords: LVGGR_GROUP, LVGGR_HEADER, LVGGR_LABEL, LVGGR_SUBSETLINK, ListView_GetGroupRect, ListView_GetGroupRect macro [Windows Controls], _shell_ListView_GetGroupRect, _shell_ListView_GetGroupRect_cpp, commctrl/ListView_GetGroupRect, controls.ListView_GetGroupRect, controls._shell_ListView_GetGroupRect
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
 - ListView_GetGroupRect
 - commctrl/ListView_GetGroupRect
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
 - ListView_GetGroupRect
---

# ListView_GetGroupRect macro

## -syntax

```cpp
BOOL ListView_GetGroupRect(
  [in]      HWND hwnd,
  [in]      int  iGroupId,
  [in]      LONG type,
  [in, out] RECT *prc
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Gets the rectangle for a specified group. Use this macro or send the <a href="/windows/desktop/Controls/lvm-getgrouprect">LVM_GETGROUPRECT</a> message explicitly.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param iGroupId [in]

Type: <b>int</b>

Specifies the group by <b>iGroupId</b> (see <a href="/windows/desktop/api/commctrl/ns-commctrl-lvgroup">LVGROUP</a> structure).

### -param type [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

Specifies the type of rectangle to retrieve. This parameter must be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVGGR_GROUP"></a><a id="lvggr_group"></a><dl>
<dt><b>LVGGR_GROUP</b></dt>
</dl>
</td>
<td width="60%">
 Coordinates of the entire expanded group.

</td>
</tr>
<tr>
<td width="40%"><a id="LVGGR_HEADER"></a><a id="lvggr_header"></a><dl>
<dt><b>LVGGR_HEADER</b></dt>
</dl>
</td>
<td width="60%">
 Coordinates of the header only (collapsed group).

</td>
</tr>
<tr>
<td width="40%"><a id="LVGGR_LABEL"></a><a id="lvggr_label"></a><dl>
<dt><b>LVGGR_LABEL</b></dt>
</dl>
</td>
<td width="60%">
 Coordinates of the label only.

</td>
</tr>
<tr>
<td width="40%"><a id="LVGGR_SUBSETLINK"></a><a id="lvggr_subsetlink"></a><dl>
<dt><b>LVGGR_SUBSETLINK</b></dt>
</dl>
</td>
<td width="60%">
 Coordinates of the subset link only (markup subset). A list-view control can limit the number of visible items displayed in each group.  A link is presented to the user to allow the user to expand the group.  This flag will return the bounding rectangle of the subset link if the group is a subset (group state of LVGS_SUBSETED, see structure <a href="/windows/desktop/api/commctrl/ns-commctrl-lvgroup">LVGROUP</a>, member <b>state</b>). This flag is provided so that accessibility applications can locate the link.

</td>
</tr>
</table>

### -param prc [in, out]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure to receive information on the group specified by <i>iGroupId</i>. The message receiver is responsible for setting the structure members with information for the group specified by <i>iGroupId</i>. The calling application is responsible for allocating memory for the structure.
