---
UID: NF:commctrl.ListView_GetCheckState
title: ListView_GetCheckState macro (commctrl.h)
description: Determines if an item in a list-view control is selected. This should be used only for list-view controls that have the LVS_EX_CHECKBOXES style.
helpviewer_keywords: ["ListView_GetCheckState","ListView_GetCheckState macro [Windows Controls]","_win32_ListView_GetCheckState","_win32_ListView_GetCheckState_cpp","commctrl/ListView_GetCheckState","controls.ListView_GetCheckState","controls._win32_ListView_GetCheckState"]
old-location: controls\ListView_GetCheckState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getcheckstate.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetCheckState, ListView_GetCheckState macro [Windows Controls], _win32_ListView_GetCheckState, _win32_ListView_GetCheckState_cpp, commctrl/ListView_GetCheckState, controls.ListView_GetCheckState, controls._win32_ListView_GetCheckState
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
 - ListView_GetCheckState
 - commctrl/ListView_GetCheckState
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
 - ListView_GetCheckState
---

# ListView_GetCheckState macro

## -syntax

```cpp
BOOL ListView_GetCheckState(
   HWND hwndLV,
   UINT i
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns nonzero if the given item is selected, or zero otherwise. If this macro is applied to a list-view control that does not have check boxes enabled, the return value is not reliable.


## -description

Determines if an item in a list-view control is selected. This should be used only for list-view controls that have the <a href="/windows/desktop/Controls/extended-list-view-styles">LVS_EX_CHECKBOXES</a> style.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a list-view control.

### -param i

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the item for which to retrieve the check state.
