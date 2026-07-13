---
UID: NF:commctrl.TreeView_GetItemRect
title: TreeView_GetItemRect macro (commctrl.h)
description: Retrieves the bounding rectangle for a tree-view item and indicates whether the item is visible. You can use this macro or send the TVM_GETITEMRECT message explicitly.
helpviewer_keywords: ["TreeView_GetItemRect","TreeView_GetItemRect macro [Windows Controls]","_win32_TreeView_GetItemRect","_win32_TreeView_GetItemRect_cpp","commctrl/TreeView_GetItemRect","controls.TreeView_GetItemRect","controls._win32_TreeView_GetItemRect"]
old-location: controls\TreeView_GetItemRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getitemrect.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetItemRect, TreeView_GetItemRect macro [Windows Controls], _win32_TreeView_GetItemRect, _win32_TreeView_GetItemRect_cpp, commctrl/TreeView_GetItemRect, controls.TreeView_GetItemRect, controls._win32_TreeView_GetItemRect
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
 - TreeView_GetItemRect
 - commctrl/TreeView_GetItemRect
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
 - TreeView_GetItemRect
---

# TreeView_GetItemRect macro

## -syntax

```cpp
BOOL TreeView_GetItemRect(
   HWND      hwnd,
   HTREEITEM hitem,
   LPRECT    prc,
   BOOL      code
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

If the item is visible and the bounding rectangle is successfully retrieved, the return value is <b>TRUE</b>. Otherwise, the <b>TVM_GETITEMRECT</b> message returns <b>FALSE</b> and does not retrieve the bounding rectangle.


## -description

Retrieves the bounding rectangle for a tree-view item and indicates whether the item is visible. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-getitemrect">TVM_GETITEMRECT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param hitem

Type: <b>HTREEITEM</b>

Handle to the tree-view item.

### -param prc

Type: <b>LPRECT</b>

Pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that receives the bounding rectangle. The coordinates are relative to the upper-left corner of the tree-view control.

### -param code

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Value specifying the portion of the item for which to retrieve the bounding rectangle. If this parameter is <b>TRUE</b>, the bounding rectangle includes only the text of the item. Otherwise, it includes the entire line that the item occupies in the tree-view control.
