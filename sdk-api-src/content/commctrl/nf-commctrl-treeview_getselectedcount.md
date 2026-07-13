---
UID: NF:commctrl.TreeView_GetSelectedCount
title: TreeView_GetSelectedCount macro (commctrl.h)
description: TreeView_GetSelectedCount macro
helpviewer_keywords: ["TreeView_GetSelectedCount","TreeView_GetSelectedCount macro [Windows Controls]","_shell_TreeView_GetSelectedCount","_shell_TreeView_GetSelectedCount_cpp","commctrl/TreeView_GetSelectedCount","controls.TreeView_GetSelectedCount","controls._shell_TreeView_GetSelectedCount"]
old-location: controls\TreeView_GetSelectedCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getselectedcount.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetSelectedCount, TreeView_GetSelectedCount macro [Windows Controls], _shell_TreeView_GetSelectedCount, _shell_TreeView_GetSelectedCount_cpp, commctrl/TreeView_GetSelectedCount, controls.TreeView_GetSelectedCount, controls._shell_TreeView_GetSelectedCount
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
 - TreeView_GetSelectedCount
 - commctrl/TreeView_GetSelectedCount
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
 - TreeView_GetSelectedCount
---

# TreeView_GetSelectedCount macro

## -syntax

```cpp
DWORD TreeView_GetSelectedCount(
  [in] HWND hwnd
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns the number of items selected.


## -description

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.
