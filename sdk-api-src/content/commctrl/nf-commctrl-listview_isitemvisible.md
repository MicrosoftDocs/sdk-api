---
UID: NF:commctrl.ListView_IsItemVisible
title: ListView_IsItemVisible macro (commctrl.h)
description: Indicates whether an item in the list-view control is visible. Use this macro or send the LVM_ISITEMVISIBLE message explicitly.
helpviewer_keywords: ["ListView_IsItemVisible","ListView_IsItemVisible macro [Windows Controls]","_shell_ListView_IsItemVisible","_shell_ListView_IsItemVisible_cpp","commctrl/ListView_IsItemVisible","controls.ListView_IsItemVisible","controls._shell_ListView_IsItemVisible"]
old-location: controls\ListView_IsItemVisible.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_isitemvisible.htm
ms.date: 10/21/2024
ms.keywords: ListView_IsItemVisible, ListView_IsItemVisible macro [Windows Controls], _shell_ListView_IsItemVisible, _shell_ListView_IsItemVisible_cpp, commctrl/ListView_IsItemVisible, controls.ListView_IsItemVisible, controls._shell_ListView_IsItemVisible
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
 - ListView_IsItemVisible
 - commctrl/ListView_IsItemVisible
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
 - ListView_IsItemVisible
---

# ListView_IsItemVisible macro

## -syntax

```cpp
UINT ListView_IsItemVisible(
  [in] HWND hwnd,
  [in] UINT index
);
```

## -returns

Type: **[UINT](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if visible, or <b>FALSE</b> otherwise.


## -description

Indicates whether an item in the list-view control is visible. Use this macro or send the <a href="/windows/desktop/Controls/lvm-isitemvisible">LVM_ISITEMVISIBLE</a> message explicitly.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param index [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of item in list-view control.
