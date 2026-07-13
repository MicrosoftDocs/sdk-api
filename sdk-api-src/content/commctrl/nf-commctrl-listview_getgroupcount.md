---
UID: NF:commctrl.ListView_GetGroupCount
title: ListView_GetGroupCount macro (commctrl.h)
description: Gets the number of groups. You can use this macro or send the LVM_GETGROUPCOUNT message explicitly.
helpviewer_keywords: ["ListView_GetGroupCount","ListView_GetGroupCount macro [Windows Controls]","_shell_ListView_GetGroupCount","_shell_ListView_GetGroupCount_cpp","commctrl/ListView_GetGroupCount","controls.ListView_GetGroupCount","controls._shell_ListView_GetGroupCount"]
old-location: controls\ListView_GetGroupCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getgroupcount.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetGroupCount, ListView_GetGroupCount macro [Windows Controls], _shell_ListView_GetGroupCount, _shell_ListView_GetGroupCount_cpp, commctrl/ListView_GetGroupCount, controls.ListView_GetGroupCount, controls._shell_ListView_GetGroupCount
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
 - ListView_GetGroupCount
 - commctrl/ListView_GetGroupCount
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
 - ListView_GetGroupCount
---

# ListView_GetGroupCount macro

## -syntax

```cpp
int ListView_GetGroupCount(
   HWND hwnd
);
```

## -returns

Type: **int**

Returns the number of groups if successful, or -1 otherwise.


## -description

Gets the number of groups. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getgroupcount">LVM_GETGROUPCOUNT</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

## -remarks

To use <b>ListView_GetGroupCount</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
