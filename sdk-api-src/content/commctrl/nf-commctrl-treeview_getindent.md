---
UID: NF:commctrl.TreeView_GetIndent
title: TreeView_GetIndent macro (commctrl.h)
description: Retrieves the amount, in pixels, that child items are indented relative to their parent items. You can use this macro or send the TVM_GETINDENT message explicitly.
helpviewer_keywords: ["TreeView_GetIndent","TreeView_GetIndent macro [Windows Controls]","_win32_TreeView_GetIndent","_win32_TreeView_GetIndent_cpp","commctrl/TreeView_GetIndent","controls.TreeView_GetIndent","controls._win32_TreeView_GetIndent"]
old-location: controls\TreeView_GetIndent.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getindent.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetIndent, TreeView_GetIndent macro [Windows Controls], _win32_TreeView_GetIndent, _win32_TreeView_GetIndent_cpp, commctrl/TreeView_GetIndent, controls.TreeView_GetIndent, controls._win32_TreeView_GetIndent
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
 - TreeView_GetIndent
 - commctrl/TreeView_GetIndent
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
 - TreeView_GetIndent
---

# TreeView_GetIndent macro

## -syntax

```cpp
UINT TreeView_GetIndent(
   HWND hwnd
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns the amount of indentation.


## -description

Retrieves the amount, in pixels, that child items are indented relative to their parent items. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-getindent">TVM_GETINDENT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.
