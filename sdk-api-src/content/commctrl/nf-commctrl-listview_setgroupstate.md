---
UID: NF:commctrl.ListView_SetGroupState
title: ListView_SetGroupState macro (commctrl.h)
description: Sets the state for a specified group.
helpviewer_keywords: ["ListView_SetGroupState","ListView_SetGroupState macro [Windows Controls]","_shell_ListView_SetGroupState","_shell_ListView_SetGroupState_cpp","commctrl/ListView_SetGroupState","controls.ListView_SetGroupState","controls._shell_ListView_SetGroupState"]
old-location: controls\ListView_SetGroupState.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setgroupstate.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetGroupState, ListView_SetGroupState macro [Windows Controls], _shell_ListView_SetGroupState, _shell_ListView_SetGroupState_cpp, commctrl/ListView_SetGroupState, controls.ListView_SetGroupState, controls._shell_ListView_SetGroupState
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
 - ListView_SetGroupState
 - commctrl/ListView_SetGroupState
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
 - ListView_SetGroupState
---

# ListView_SetGroupState macro

## -syntax

```cpp
LRESULT ListView_SetGroupState(
  [in] HWND hwnd,
  [in] UINT dwGroupId,
  [in] UINT dwMask,
  [in] UINT dwState
);
```

## -returns

Type: **[LRESULT](/windows/desktop/winprog/windows-data-types)**

Returns the ID of the group (<b>iGroupId</b>) if successful, or -1 otherwise.


## -description

Sets the state for a specified group.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param dwGroupId [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the group by <b>iGroupId</b> (see <a href="/windows/desktop/api/commctrl/ns-commctrl-lvgroup">LVGROUP</a> structure).

### -param dwMask [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the state values to set or clear. This is a combination of the flags listed for the <b>state</b> member of <a href="/windows/desktop/api/commctrl/ns-commctrl-lvgroup">LVGROUP</a>.

### -param dwState [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Specifies the state values to set. States that are not included here but are included in <i>dwMask</i> are cleared.

## -remarks

<div class="alert"><b>Note</b>  To use this macro, you must provide a manifest specifying Comctl32.dll version 6.0. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.</div>
<div> </div>
You can also set the group state by using <a href="/windows/desktop/api/commctrl/nf-commctrl-listview_setgroupinfo">ListView_SetGroupInfo</a>.
