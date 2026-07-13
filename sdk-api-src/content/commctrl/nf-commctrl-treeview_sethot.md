---
UID: NF:commctrl.TreeView_SetHot
title: TreeView_SetHot macro (commctrl.h)
description: Sets the hot item for a tree-view control. You can use this macro or send the TVM_SETHOT message explicitly.
helpviewer_keywords: ["TreeView_SetHot","TreeView_SetHot macro [Windows Controls]","_win32_TreeView_SetHot","_win32_TreeView_SetHot_cpp","commctrl/TreeView_SetHot","controls.TreeView_SetHot","controls._win32_TreeView_SetHot"]
old-location: controls\TreeView_SetHot.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\messages\treeview_sethot.htm
ms.date: 10/21/2024
ms.keywords: TreeView_SetHot, TreeView_SetHot macro [Windows Controls], _win32_TreeView_SetHot, _win32_TreeView_SetHot_cpp, commctrl/TreeView_SetHot, controls.TreeView_SetHot, controls._win32_TreeView_SetHot
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
 - TreeView_SetHot
 - commctrl/TreeView_SetHot
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
 - TreeView_SetHot
---

# TreeView_SetHot macro

## -syntax

```cpp
LRESULT TreeView_SetHot(
   HWND      hwnd,
   HTREEITEM hitem
);
```

## -returns

Type: **[LRESULT](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

<p class="CCE_Message">[Intended for internal use; not recommended for use in applications. This macro may not be supported in future versions of Windows.]

Sets the hot item for a tree-view control. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-sethot">TVM_SETHOT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param hitem

Type: <b>HTREEITEM</b>

Handle to the new hot item. If this value is <b>NULL</b>, the tree-view control will be set to have no hot item.

## -remarks

The <i>hot item</i> is the item that the mouse is hovering over. The <a href="/windows/desktop/Controls/tvm-sethot">TVM_SETHOT</a> message sent by this macro makes an item look like it is the hot item even if the mouse is not hovering over it.

The <a href="/windows/desktop/Controls/tvm-sethot">TVM_SETHOT</a> message has no visible effect if the <a href="/windows/desktop/Controls/tree-view-control-window-styles">TVS_TRACKSELECT</a> style is not set.

If it succeeds, the <a href="/windows/desktop/Controls/tvm-sethot">TVM_SETHOT</a> message causes the hot item to be redrawn.

The <a href="/windows/desktop/Controls/tvm-sethot">TVM_SETHOT</a> message is ignored if <i>hitem</i> is <b>NULL</b> and the tree-view control is tracking the mouse.

## -see-also

<a href="/windows/desktop/Controls/tvm-sethot">TVM_SETHOT</a>
