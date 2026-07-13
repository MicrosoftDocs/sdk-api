---
UID: NF:commctrl.TreeView_SelectSetFirstVisible
title: TreeView_SelectSetFirstVisible macro (commctrl.h)
description: Scrolls the tree-view control vertically to ensure that the specified item is visible.
helpviewer_keywords: ["TreeView_SelectSetFirstVisible","TreeView_SelectSetFirstVisible macro [Windows Controls]","_win32_TreeView_SelectSetFirstVisible","_win32_TreeView_SelectSetFirstVisible_cpp","commctrl/TreeView_SelectSetFirstVisible","controls.TreeView_SelectSetFirstVisible","controls._win32_TreeView_SelectSetFirstVisible"]
old-location: controls\TreeView_SelectSetFirstVisible.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_selectsetfirstvisible.htm
ms.date: 10/21/2024
ms.keywords: TreeView_SelectSetFirstVisible, TreeView_SelectSetFirstVisible macro [Windows Controls], _win32_TreeView_SelectSetFirstVisible, _win32_TreeView_SelectSetFirstVisible_cpp, commctrl/TreeView_SelectSetFirstVisible, controls.TreeView_SelectSetFirstVisible, controls._win32_TreeView_SelectSetFirstVisible
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
 - TreeView_SelectSetFirstVisible
 - commctrl/TreeView_SelectSetFirstVisible
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
 - TreeView_SelectSetFirstVisible
---

# TreeView_SelectSetFirstVisible macro

## -syntax

```cpp
BOOL TreeView_SelectSetFirstVisible(
   HWND      hwnd,
   HTREEITEM hitem
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Scrolls the tree-view control vertically to ensure that the specified item is visible. If possible, the specified item becomes the first visible item at the top of the control's window. You can use this macro or the <a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_select">TreeView_Select</a> macro, or you can send the <a href="/windows/desktop/Controls/tvm-selectitem">TVM_SELECTITEM</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param hitem

Type: <b>HTREEITEM</b>

Handle to an item. If the <i>hitem</i> parameter is <b>NULL</b>, the control is set to have no selected item.

## -remarks

Tree-view controls display as many items as will fit in the window. If the specified item is near the bottom of the control's hierarchy of items, it might not become the first visible item, depending on how many items fit in the window. 

If the specified item is the child of a collapsed parent item, the parent's list of child items is expanded to reveal the specified item. In this case, the parent window receives the <a href="/windows/desktop/Controls/tvn-itemexpanding">TVN_ITEMEXPANDING</a> and <a href="/windows/desktop/Controls/tvn-itemexpanded">TVN_ITEMEXPANDED</a> notification codes. 

Using the <b>TreeView_SelectSetFirstVisible</b> macro is equivalent to sending the <a href="/windows/desktop/Controls/tvm-selectitem">TVM_SELECTITEM</a> message with its <i>flag</i> parameter set to the TVGN_FIRSTVISIBLE value.
