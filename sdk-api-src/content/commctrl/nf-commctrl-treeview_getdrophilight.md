---
UID: NF:commctrl.TreeView_GetDropHilight
title: TreeView_GetDropHilight macro (commctrl.h)
description: Retrieves the tree-view item that is the target of a drag-and-drop operation. You can use this macro, or you can explicitly send the TVM_GETNEXTITEM message with the TVGN_DROPHILITE flag.
helpviewer_keywords: ["TreeView_GetDropHilight","TreeView_GetDropHilight macro [Windows Controls]","_win32_TreeView_GetDropHilight","_win32_TreeView_GetDropHilight_cpp","commctrl/TreeView_GetDropHilight","controls.TreeView_GetDropHilight","controls._win32_TreeView_GetDropHilight"]
old-location: controls\TreeView_GetDropHilight.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getdrophilight.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetDropHilight, TreeView_GetDropHilight macro [Windows Controls], _win32_TreeView_GetDropHilight, _win32_TreeView_GetDropHilight_cpp, commctrl/TreeView_GetDropHilight, controls.TreeView_GetDropHilight, controls._win32_TreeView_GetDropHilight
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
 - TreeView_GetDropHilight
 - commctrl/TreeView_GetDropHilight
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
 - TreeView_GetDropHilight
---

# TreeView_GetDropHilight macro

## -syntax

```cpp
HTREEITEM TreeView_GetDropHilight(
   HWND hwnd
);
```

## -returns

Type: **HTREEITEM**

Returns the handle to the item if successful, or <b>NULL</b> otherwise.


## -description

Retrieves the tree-view item that is the target of a drag-and-drop operation. You can use this macro, or you can explicitly send the <a href="/windows/desktop/Controls/tvm-getnextitem">TVM_GETNEXTITEM</a> message with the TVGN_DROPHILITE flag.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.
