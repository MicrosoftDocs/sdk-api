---
UID: NF:commctrl.TreeView_HitTest
title: TreeView_HitTest macro (commctrl.h)
description: Determines the location of the specified point relative to the client area of a tree-view control. You can use this macro or send the TVM_HITTEST message explicitly.
helpviewer_keywords: ["TreeView_HitTest","TreeView_HitTest macro [Windows Controls]","_win32_TreeView_HitTest","_win32_TreeView_HitTest_cpp","commctrl/TreeView_HitTest","controls.TreeView_HitTest","controls._win32_TreeView_HitTest"]
old-location: controls\TreeView_HitTest.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_hittest.htm
ms.date: 10/21/2024
ms.keywords: TreeView_HitTest, TreeView_HitTest macro [Windows Controls], _win32_TreeView_HitTest, _win32_TreeView_HitTest_cpp, commctrl/TreeView_HitTest, controls.TreeView_HitTest, controls._win32_TreeView_HitTest
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
 - TreeView_HitTest
 - commctrl/TreeView_HitTest
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
 - TreeView_HitTest
---

# TreeView_HitTest macro

## -syntax

```cpp
HTREEITEM TreeView_HitTest(
   HWND            hwnd,
   LPTVHITTESTINFO lpht
);
```

## -returns

Type: **HTREEITEM**

Returns the handle to the tree-view item that occupies the specified point, or <b>NULL</b> if no item occupies the point.


## -description

Determines the location of the specified point relative to the client area of a tree-view control. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-hittest">TVM_HITTEST</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

### -param lpht

Type: <b>LPTVHITTESTINFO</b>

Pointer to a <a href="/windows/desktop/api/commctrl/ns-commctrl-tvhittestinfo">TVHITTESTINFO</a> structure. When the message is sent, the <b>pt</b> member specifies the coordinates of the point to test. When the message returns, the <b>hItem</b> member is the handle to the item at the specified point or <b>NULL</b> if no item occupies the point. Also, when the message returns, the <b>flags</b> member is a hit test value that indicates the location of the specified point. For a list of hit test values, see the description of the <b>TVHITTESTINFO</b> structure.
