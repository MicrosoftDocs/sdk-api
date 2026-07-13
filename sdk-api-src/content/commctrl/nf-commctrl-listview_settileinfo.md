---
UID: NF:commctrl.ListView_SetTileInfo
title: ListView_SetTileInfo macro (commctrl.h)
description: Sets information for an existing tile of a list-view control. You can use this macro or send the LVM_SETTILEINFO message explicitly.
helpviewer_keywords: ["ListView_SetTileInfo","ListView_SetTileInfo macro [Windows Controls]","_win32_ListView_SetTileInfo","_win32_ListView_SetTileInfo_cpp","commctrl/ListView_SetTileInfo","controls.ListView_SetTileInfo","controls._win32_ListView_SetTileInfo"]
old-location: controls\ListView_SetTileInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_settileinfo.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetTileInfo, ListView_SetTileInfo macro [Windows Controls], _win32_ListView_SetTileInfo, _win32_ListView_SetTileInfo_cpp, commctrl/ListView_SetTileInfo, controls.ListView_SetTileInfo, controls._win32_ListView_SetTileInfo
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
 - ListView_SetTileInfo
 - commctrl/ListView_SetTileInfo
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
 - ListView_SetTileInfo
---

# ListView_SetTileInfo macro

## -syntax

```cpp
BOOL ListView_SetTileInfo(
   HWND        hwnd,
   PLVTILEINFO pti
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Sets information for an existing tile of a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-settileinfo">LVM_SETTILEINFO</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param pti

Type: <b>PLVTILEINFO</b>

<a href="/windows/desktop/api/commctrl/ns-commctrl-lvtileinfo">LVTILEINFO</a>

## -remarks

To use <b>ListView_SetTileInfo</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
