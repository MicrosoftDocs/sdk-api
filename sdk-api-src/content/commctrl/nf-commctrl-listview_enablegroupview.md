---
UID: NF:commctrl.ListView_EnableGroupView
title: ListView_EnableGroupView macro (commctrl.h)
description: Enables or disables whether the items in a list-view control display as a group. You can use this macro or send the LVM_ENABLEGROUPVIEW message explicitly.
helpviewer_keywords: ["ListView_EnableGroupView","ListView_EnableGroupView macro [Windows Controls]","_win32_ListView_EnableGroupView","_win32_ListView_EnableGroupView_cpp","commctrl/ListView_EnableGroupView","controls.ListView_EnableGroupView","controls._win32_ListView_EnableGroupView"]
old-location: controls\ListView_EnableGroupView.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_enablegroupview.htm
ms.date: 10/21/2024
ms.keywords: ListView_EnableGroupView, ListView_EnableGroupView macro [Windows Controls], _win32_ListView_EnableGroupView, _win32_ListView_EnableGroupView_cpp, commctrl/ListView_EnableGroupView, controls.ListView_EnableGroupView, controls._win32_ListView_EnableGroupView
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
 - ListView_EnableGroupView
 - commctrl/ListView_EnableGroupView
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
 - ListView_EnableGroupView
---

# ListView_EnableGroupView macro

## -syntax

```cpp
int ListView_EnableGroupView(
   HWND hwnd,
   BOOL fEnable
);
```

## -returns

Type: **int**

Returns one of the following values:

| Return code | Description |
|---|---|
| 0 | The ability to display list-view items as a group is already enabled or disabled. |
| 1 | The state of the control was successfully changed. |
| -1 | The operation failed. |



## -description

Enables or disables whether the items in a list-view control display as a group. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-enablegroupview">LVM_ENABLEGROUPVIEW</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param fEnable

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>BOOL</b>
<b>TRUE</b>
<b>FALSE</b>

## -remarks

To use <b>ListView_EnableGroupView</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
