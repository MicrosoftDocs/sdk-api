---
UID: NF:commctrl.TreeView_GetItemPartRect
title: TreeView_GetItemPartRect macro (commctrl.h)
description: Retrieves the largest possible bounding rectangle that constitutes the &quot;hit zone&quot; for a specified part of an item. Use this macro or send the TVM_GETITEMPARTRECT message explicitly.
helpviewer_keywords: ["TreeView_GetItemPartRect","TreeView_GetItemPartRect macro [Windows Controls]","_shell_TreeView_GetItemPartRect","_shell_TreeView_GetItemPartRect_cpp","commctrl/TreeView_GetItemPartRect","controls.TreeView_GetItemPartRect","controls._shell_TreeView_GetItemPartRect"]
old-location: controls\TreeView_GetItemPartRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getitempartrect.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetItemPartRect, TreeView_GetItemPartRect macro [Windows Controls], _shell_TreeView_GetItemPartRect, _shell_TreeView_GetItemPartRect_cpp, commctrl/TreeView_GetItemPartRect, controls.TreeView_GetItemPartRect, controls._shell_TreeView_GetItemPartRect
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
 - TreeView_GetItemPartRect
 - commctrl/TreeView_GetItemPartRect
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
 - TreeView_GetItemPartRect
---

# TreeView_GetItemPartRect macro

## -syntax

```cpp
BOOL TreeView_GetItemPartRect(
   HWND       hwnd,
   HTREEITEM  hitem,
   RECT       *prc,
   TVITEMPART *partid
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Retrieves the largest possible bounding rectangle that constitutes the "hit zone" for a specified part of an item. Use this macro or send the <a href="/windows/desktop/Controls/tvm-getitempartrect">TVM_GETITEMPARTRECT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param hitem

Type: <b>HTREEITEM</b>

Handle to the tree-view item.

### -param prc

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the bounding rectangle. The caller is responsible for allocating this structure. The coordinates received are relative to the upper-left corner of the tree-view control.

### -param partid

Type: <b>TVITEMPART*</b>

ID of the item part. This value must be <b>TVGIPR_BUTTON</b> (0x0001).

## -remarks

This message returns the largest possible bounding rectangle such that for every (x,y) coordinate within the rectangle, a click by the user at that coordinate would constitute a hit on that part of the item.
