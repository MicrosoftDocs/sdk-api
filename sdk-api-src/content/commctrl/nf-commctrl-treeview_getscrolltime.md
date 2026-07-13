---
UID: NF:commctrl.TreeView_GetScrollTime
title: TreeView_GetScrollTime macro (commctrl.h)
description: Retrieves the maximum scroll time for the tree-view control. You can use this macro or send the TVM_GETSCROLLTIME message explicitly.
helpviewer_keywords: ["TreeView_GetScrollTime","TreeView_GetScrollTime macro [Windows Controls]","_win32_TreeView_GetScrollTime","_win32_TreeView_GetScrollTime_cpp","commctrl/TreeView_GetScrollTime","controls.TreeView_GetScrollTime","controls._win32_TreeView_GetScrollTime"]
old-location: controls\TreeView_GetScrollTime.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getscrolltime.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetScrollTime, TreeView_GetScrollTime macro [Windows Controls], _win32_TreeView_GetScrollTime, _win32_TreeView_GetScrollTime_cpp, commctrl/TreeView_GetScrollTime, controls.TreeView_GetScrollTime, controls._win32_TreeView_GetScrollTime
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
 - TreeView_GetScrollTime
 - commctrl/TreeView_GetScrollTime
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
 - TreeView_GetScrollTime
---

# TreeView_GetScrollTime macro

## -syntax

```cpp
UINT TreeView_GetScrollTime(
   HWND hwnd
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns the maximum scroll time, in milliseconds.


## -description

Retrieves the maximum scroll time for the tree-view control. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-getscrolltime">TVM_GETSCROLLTIME</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the tree-view control.

## -remarks

The maximum scroll time is the longest amount of time that a scroll operation can take. Scrolling will be adjusted so that the scroll will take place within the maximum scroll time. A scroll operation may take less time than the maximum.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_setscrolltime">TreeView_SetScrollTime</a>
