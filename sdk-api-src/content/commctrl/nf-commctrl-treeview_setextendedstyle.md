---
UID: NF:commctrl.TreeView_SetExtendedStyle
title: TreeView_SetExtendedStyle macro (commctrl.h)
description: Sets the extended style for a specified TreeView control. Use this macro or send the TVM_SETEXTENDEDSTYLE message explicitly.
helpviewer_keywords: ["TreeView_SetExtendedStyle","TreeView_SetExtendedStyle macro [Windows Controls]","_shell_TreeView_SetExtendedStyle","_shell_TreeView_SetExtendedStyle_cpp","commctrl/TreeView_SetExtendedStyle","controls.TreeView_SetExtendedStyle","controls._shell_TreeView_SetExtendedStyle"]
old-location: controls\TreeView_SetExtendedStyle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_setextendedstyle.htm
ms.date: 10/21/2024
ms.keywords: TreeView_SetExtendedStyle, TreeView_SetExtendedStyle macro [Windows Controls], _shell_TreeView_SetExtendedStyle, _shell_TreeView_SetExtendedStyle_cpp, commctrl/TreeView_SetExtendedStyle, controls.TreeView_SetExtendedStyle, controls._shell_TreeView_SetExtendedStyle
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
 - TreeView_SetExtendedStyle
 - commctrl/TreeView_SetExtendedStyle
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
 - TreeView_SetExtendedStyle
---

# TreeView_SetExtendedStyle macro

## -syntax

```cpp
HRESULT TreeView_SetExtendedStyle(
   HWND  hwnd,
   DWORD dw,
   UINT  mask
);
```

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If this macro succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -description

Sets the extended style for a specified TreeView control. Use this macro or send the <a href="/windows/desktop/Controls/tvm-setextendedstyle">TVM_SETEXTENDEDSTYLE</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the TreeView control.

### -param dw

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

Value that indicates the extended style. For more information on styles, see <a href="/windows/desktop/Controls/tree-view-control-window-extended-styles">Tree-View Control Extended Styles</a>.

### -param mask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Mask used to select the styles to be set.
