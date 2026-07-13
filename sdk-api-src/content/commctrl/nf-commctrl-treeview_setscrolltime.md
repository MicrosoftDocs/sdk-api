---
UID: NF:commctrl.TreeView_SetScrollTime
title: TreeView_SetScrollTime macro (commctrl.h)
description: Sets the maximum scroll time for the tree-view control. You can use this macro or send the TVM_SETSCROLLTIME message explicitly.
helpviewer_keywords: ["TreeView_SetScrollTime","TreeView_SetScrollTime macro [Windows Controls]","_win32_TreeView_SetScrollTime","_win32_TreeView_SetScrollTime_cpp","commctrl/TreeView_SetScrollTime","controls.TreeView_SetScrollTime","controls._win32_TreeView_SetScrollTime"]
old-location: controls\TreeView_SetScrollTime.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setscrolltime.htm
ms.date: 10/21/2024
ms.keywords: TreeView_SetScrollTime, TreeView_SetScrollTime macro [Windows Controls], _win32_TreeView_SetScrollTime, _win32_TreeView_SetScrollTime_cpp, commctrl/TreeView_SetScrollTime, controls.TreeView_SetScrollTime, controls._win32_TreeView_SetScrollTime
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
 - TreeView_SetScrollTime
 - commctrl/TreeView_SetScrollTime
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
 - TreeView_SetScrollTime
---

# TreeView_SetScrollTime macro

## -syntax

```cpp
UINT TreeView_SetScrollTime(
   HWND hwnd,
   UINT uTime
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns the previous scroll time, in milliseconds.


## -description

Sets the maximum scroll time for the tree-view control. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-setscrolltime">TVM_SETSCROLLTIME</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a tree-view control.

### -param uTime

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

New maximum scroll time, in milliseconds. If this value is less than 100, it will be rounded up to 100.

## -remarks

The maximum scroll time is the longest amount of time that a scroll operation can take. Scrolling will be adjusted so that the scroll will take place within the maximum scroll time. A scroll operation may take less time than the maximum.

## -see-also

<a href="/windows/desktop/Controls/tvm-getscrolltime">TVM_GETSCROLLTIME</a>
