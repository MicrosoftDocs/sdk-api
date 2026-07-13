---
UID: NF:commctrl.TreeView_GetUnicodeFormat
title: TreeView_GetUnicodeFormat macro (commctrl.h)
description: Retrieves the Unicode character format flag for the control. You can use this macro or send the TVM_GETUNICODEFORMAT message explicitly.
helpviewer_keywords: ["TreeView_GetUnicodeFormat","TreeView_GetUnicodeFormat macro [Windows Controls]","_win32_TreeView_GetUnicodeFormat","_win32_TreeView_GetUnicodeFormat_cpp","commctrl/TreeView_GetUnicodeFormat","controls.TreeView_GetUnicodeFormat","controls._win32_TreeView_GetUnicodeFormat"]
old-location: controls\TreeView_GetUnicodeFormat.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\treeview\macros\treeview_getunicodeformat.htm
ms.date: 10/21/2024
ms.keywords: TreeView_GetUnicodeFormat, TreeView_GetUnicodeFormat macro [Windows Controls], _win32_TreeView_GetUnicodeFormat, _win32_TreeView_GetUnicodeFormat_cpp, commctrl/TreeView_GetUnicodeFormat, controls.TreeView_GetUnicodeFormat, controls._win32_TreeView_GetUnicodeFormat
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
 - TreeView_GetUnicodeFormat
 - commctrl/TreeView_GetUnicodeFormat
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
 - TreeView_GetUnicodeFormat
---

# TreeView_GetUnicodeFormat macro

## -syntax

```cpp
BOOL TreeView_GetUnicodeFormat(
   HWND hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns the Unicode format flag for the control. If this value is nonzero, the control is using Unicode characters. If this value is zero, the control is using ANSI characters.


## -description

Retrieves the Unicode character format flag for the control. You can use this macro or send the <a href="/windows/desktop/Controls/tvm-getunicodeformat">TVM_GETUNICODEFORMAT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to the control.

## -see-also

<a href="/windows/desktop/api/commctrl/nf-commctrl-treeview_setunicodeformat">TreeView_SetUnicodeFormat</a>
