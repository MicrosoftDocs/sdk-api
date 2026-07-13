---
UID: NF:commctrl.TreeView_GetToolTips
title: TreeView_GetToolTips macro (commctrl.h)
description: Retrieves the handle to the child tooltip control used by a tree-view control. You can use this macro or send the TVM_GETTOOLTIPS message explicitly.
helpviewer_keywords: ["TreeView_GetToolTips","TreeView_GetToolTips macro [Windows Controls]","_win32_TreeView_GetToolTips","_win32_TreeView_GetToolTips_cpp","commctrl/TreeView_GetToolTips","controls.TreeView_GetToolTips","controls._win32_TreeView_GetToolTips"]
old-location: controls\TreeView_GetToolTips.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_gettooltips.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetToolTips, TreeView_GetToolTips macro [Windows Controls], _win32_TreeView_GetToolTips, _win32_TreeView_GetToolTips_cpp, commctrl/TreeView_GetToolTips, controls.TreeView_GetToolTips, controls._win32_TreeView_GetToolTips
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
 - TreeView_GetToolTips
 - commctrl/TreeView_GetToolTips
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
 - TreeView_GetToolTips
---

# TreeView_GetToolTips macro

## -syntax

```cpp
HWND TreeView_GetToolTips(
   HWND hwnd
);
```

## -returns

Type: **[HWND](/windows/desktop/winprog/windows-data-types)**

Returns the handle to the child tooltip control, or <b>NULL</b> if the control is not using tooltips.


## -description

Retrieves the handle to the child tooltip control used by a tree-view control. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-gettooltips">TVM_GETTOOLTIPS</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a tree-view control.

## -remarks

When created, tree-view controls automatically create a child tooltip control. To prevent a tree-view control from using tooltips, create the control with the <a href="/windows/desktop/Controls/tree-view-control-window-styles">TVS_NOTOOLTIPS</a> style.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_settooltips">TreeView_SetToolTips</a>
