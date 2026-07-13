---
UID: NF:commctrl.ListView_SetItemIndexState
title: ListView_SetItemIndexState macro (commctrl.h)
description: Sets the state of a specified list-view item. Use this macro or send the LVM_SETITEMINDEXSTATE message explicitly.
helpviewer_keywords: ["ListView_SetItemIndexState","ListView_SetItemIndexState macro [Windows Controls]","_shell_ListView_SetItemIndexState","_shell_ListView_SetItemIndexState_cpp","commctrl/ListView_SetItemIndexState","controls.ListView_SetItemIndexState","controls._shell_ListView_SetItemIndexState"]
old-location: controls\ListView_SetItemIndexState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setitemindexstate.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetItemIndexState, ListView_SetItemIndexState macro [Windows Controls], _shell_ListView_SetItemIndexState, _shell_ListView_SetItemIndexState_cpp, commctrl/ListView_SetItemIndexState, controls.ListView_SetItemIndexState, controls._shell_ListView_SetItemIndexState
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
 - ListView_SetItemIndexState
 - commctrl/ListView_SetItemIndexState
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
 - ListView_SetItemIndexState
---

# ListView_SetItemIndexState macro

## -syntax

```cpp
HRESULT ListView_SetItemIndexState(
  [in] HWND        hwndLV,
  [in] LVITEMINDEX *plvii,
  [in] UINT        data,
  [in] UINT        mask
);
```

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

Returns one of the following values of type <b>HRESULT</b>.

| Return code | Description |
|---|---|
| E_FAIL | The state could not be set. |
| E_UNEXPECTED | The list-view control was not ready for the operation. |
| S_OK | The operation was successful. |


## -description

Sets the state of a specified list-view item. Use this macro or send the <a href="/windows/desktop/Controls/lvm-setitemindexstate">LVM_SETITEMINDEXSTATE</a> message explicitly.

## -parameters

### -param hwndLV [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param plvii [in]

Type: <b><a href="/windows/desktop/api/commctrl/ns-commctrl-lvitemindex">LVITEMINDEX</a>*</b>

A pointer to an <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitemindex">LVITEMINDEX</a> structure for the item. The caller is responsible for allocating this structure and setting the members.

### -param data [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The state to set on the item as one or more (as a bitwise combination) of the <a href="/windows/desktop/Controls/list-view-item-states">List-View Item States</a> flags.

### -param mask [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The valid bits of the state specified by parameter <i>data</i>. For more information, see the <i>stateMask</i> member of the <a href="/windows/desktop/api/commctrl/ns-commctrl-lvitema">LVITEM</a>) structure.
