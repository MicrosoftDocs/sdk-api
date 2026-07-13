---
UID: NF:commctrl.ListView_SetTileViewInfo
title: ListView_SetTileViewInfo macro (commctrl.h)
description: Sets information that a list-view control uses in tile view. You can use this macro or send the LVM_SETTILEVIEWINFO message explicitly.
helpviewer_keywords: ["ListView_SetTileViewInfo","ListView_SetTileViewInfo macro [Windows Controls]","_win32_ListView_SetTileViewInfo","_win32_ListView_SetTileViewInfo_cpp","commctrl/ListView_SetTileViewInfo","controls.ListView_SetTileViewInfo","controls._win32_ListView_SetTileViewInfo"]
old-location: controls\ListView_SetTileViewInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_settileviewinfo.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetTileViewInfo, ListView_SetTileViewInfo macro [Windows Controls], _win32_ListView_SetTileViewInfo, _win32_ListView_SetTileViewInfo_cpp, commctrl/ListView_SetTileViewInfo, controls.ListView_SetTileViewInfo, controls._win32_ListView_SetTileViewInfo
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
 - ListView_SetTileViewInfo
 - commctrl/ListView_SetTileViewInfo
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
 - ListView_SetTileViewInfo
---

# ListView_SetTileViewInfo macro

## -syntax

```cpp
BOOL ListView_SetTileViewInfo(
   HWND            hwnd,
   PLVTILEVIEWINFO ptvi
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.


## -description

Sets information that a list-view control uses in tile view. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-settileviewinfo">LVM_SETTILEVIEWINFO</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param ptvi

Type: <b>PLVTILEVIEWINFO</b>

<a href="/windows/desktop/api/commctrl/ns-commctrl-lvtileviewinfo">LVTILEVIEWINFO</a>

## -remarks

To use <b>ListView_SetTileViewInfo</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
