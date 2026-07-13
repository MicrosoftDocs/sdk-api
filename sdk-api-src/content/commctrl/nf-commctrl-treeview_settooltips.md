---
UID: NF:commctrl.TreeView_SetToolTips
title: TreeView_SetToolTips macro (commctrl.h)
description: Sets a tree-view control's child tooltip control. You can use this macro or send the TVM_SETTOOLTIPS message explicitly.
helpviewer_keywords: ["TreeView_SetToolTips","TreeView_SetToolTips macro [Windows Controls]","_win32_TreeView_SetToolTips","_win32_TreeView_SetToolTips_cpp","commctrl/TreeView_SetToolTips","controls.TreeView_SetToolTips","controls._win32_TreeView_SetToolTips"]
old-location: controls\TreeView_SetToolTips.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_settooltips.htm
ms.date: 10/21/2024
ms.keywords: TreeView_SetToolTips, TreeView_SetToolTips macro [Windows Controls], _win32_TreeView_SetToolTips, _win32_TreeView_SetToolTips_cpp, commctrl/TreeView_SetToolTips, controls.TreeView_SetToolTips, controls._win32_TreeView_SetToolTips
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
 - TreeView_SetToolTips
 - commctrl/TreeView_SetToolTips
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
 - TreeView_SetToolTips
---

# TreeView_SetToolTips macro

## -syntax

```cpp
HWND TreeView_SetToolTips(
   HWND hwnd,
   HWND hwndTT
);
```

## -returns

Type: **[HWND](/windows/desktop/winprog/windows-data-types)**

Returns the handle to tooltip control previously set for the tree-view control, or <b>NULL</b> if tooltips were not previously used.


## -description

Sets a tree-view control's child tooltip control. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-settooltips">TVM_SETTOOLTIPS</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a tree-view control.

### -param hwndTT

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a tooltip control.

## -remarks

When created, tree-view controls automatically create a child tooltip control. To prevent a tree-view control from using tooltips, create the control with the <a href="/windows/desktop/Controls/tree-view-control-window-styles">TVS_NOTOOLTIPS</a> style.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_gettooltips">TreeView_GetToolTips</a>
