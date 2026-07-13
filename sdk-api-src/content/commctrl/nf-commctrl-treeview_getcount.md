---
UID: NF:commctrl.TreeView_GetCount
title: TreeView_GetCount macro (commctrl.h)
description: Retrieves a count of the items in a tree-view control. You can use this macro or send the TVM_GETCOUNT message explicitly.
helpviewer_keywords: ["TreeView_GetCount","TreeView_GetCount macro [Windows Controls]","_win32_TreeView_GetCount","_win32_TreeView_GetCount_cpp","commctrl/TreeView_GetCount","controls.TreeView_GetCount","controls._win32_TreeView_GetCount"]
old-location: controls\TreeView_GetCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getcount.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetCount, TreeView_GetCount macro [Windows Controls], _win32_TreeView_GetCount, _win32_TreeView_GetCount_cpp, commctrl/TreeView_GetCount, controls.TreeView_GetCount, controls._win32_TreeView_GetCount
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
 - TreeView_GetCount
 - commctrl/TreeView_GetCount
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
 - TreeView_GetCount
---

# TreeView_GetCount macro

## -syntax

```cpp
UINT TreeView_GetCount(
   HWND hwnd
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns the count of items.


## -description

Retrieves a count of the items in a tree-view control. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-getcount">TVM_GETCOUNT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

## -remarks

The node count returned by <b>TreeView_GetCount</b> is limited to integer values. If you add a node beyond 32767 the macro returns a negative value. After adding 65536 nodes the count returns to zero. When this occurs, the tree-view control appears empty with no scrollbars. For more information see the Knowledge Base article <a href="https://support.microsoft.com/default.aspx?scid=kb;en-us;Q182231">Q182231</a>.
