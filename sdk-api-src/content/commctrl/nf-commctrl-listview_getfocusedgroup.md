---
UID: NF:commctrl.ListView_GetFocusedGroup
title: ListView_GetFocusedGroup macro (commctrl.h)
description: Gets the group that has the focus. Use this macro or send the LVM_GETFOCUSEDGROUP message explicitly.
helpviewer_keywords: ["ListView_GetFocusedGroup","ListView_GetFocusedGroup macro [Windows Controls]","_shell_ListView_GetFocusedGroup","_shell_ListView_GetFocusedGroup_cpp","commctrl/ListView_GetFocusedGroup","controls.ListView_GetFocusedGroup","controls._shell_ListView_GetFocusedGroup"]
old-location: controls\ListView_GetFocusedGroup.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getfocusedgroup.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetFocusedGroup, ListView_GetFocusedGroup macro [Windows Controls], _shell_ListView_GetFocusedGroup, _shell_ListView_GetFocusedGroup_cpp, commctrl/ListView_GetFocusedGroup, controls.ListView_GetFocusedGroup, controls._shell_ListView_GetFocusedGroup
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
 - ListView_GetFocusedGroup
 - commctrl/ListView_GetFocusedGroup
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
 - ListView_GetFocusedGroup
---

# ListView_GetFocusedGroup macro

## -syntax

```cpp
INT ListView_GetFocusedGroup(
  [in] HWND hwnd
);
```

## -returns

Type: **[INT](/windows/desktop/winprog/windows-data-types)**

Returns the index of the group with state of LVGS_FOCUSED, or -1 if there is no group with state of LVGS_FOCUSED.


## -description

Gets the group that has the focus. Use this macro or send the <a href="/windows/desktop/Controls/lvm-getfocusedgroup">LVM_GETFOCUSEDGROUP</a> message explicitly.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.
