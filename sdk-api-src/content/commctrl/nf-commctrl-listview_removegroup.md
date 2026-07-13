---
UID: NF:commctrl.ListView_RemoveGroup
title: ListView_RemoveGroup macro (commctrl.h)
description: Removes a group from a list-view control. You can use this macro or send the LVM_REMOVEGROUP message explicitly.
helpviewer_keywords: ["ListView_RemoveGroup","ListView_RemoveGroup macro [Windows Controls]","_win32_ListView_RemoveGroup","_win32_ListView_RemoveGroup_cpp","commctrl/ListView_RemoveGroup","controls.ListView_RemoveGroup","controls._win32_ListView_RemoveGroup"]
old-location: controls\ListView_RemoveGroup.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_removegroup.htm
ms.date: 10/21/2024
ms.keywords: ListView_RemoveGroup, ListView_RemoveGroup macro [Windows Controls], _win32_ListView_RemoveGroup, _win32_ListView_RemoveGroup_cpp, commctrl/ListView_RemoveGroup, controls.ListView_RemoveGroup, controls._win32_ListView_RemoveGroup
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
 - ListView_RemoveGroup
 - commctrl/ListView_RemoveGroup
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
 - ListView_RemoveGroup
---

# ListView_RemoveGroup macro

## -syntax

```cpp
int ListView_RemoveGroup(
   HWND hwnd,
   int  iGroupId
);
```

## -returns

Type: **int**

Returns the index of the group if successful, or -1 otherwise.


## -description

Removes a group from a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-removegroup">LVM_REMOVEGROUP</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param iGroupId

Type: <b>int</b>

## -remarks

To use <b>ListView_RemoveGroup</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
