---
UID: NF:commctrl.ListView_GetTileInfo
title: ListView_GetTileInfo macro (commctrl.h)
description: Gets information about a tile in a list-view control. You can use this macro or send the LVM_GETTILEINFO message explicitly.
helpviewer_keywords: ["ListView_GetTileInfo","ListView_GetTileInfo macro [Windows Controls]","_win32_ListView_GetTileInfo","_win32_ListView_GetTileInfo_cpp","commctrl/ListView_GetTileInfo","controls.ListView_GetTileInfo","controls._win32_ListView_GetTileInfo"]
old-location: controls\ListView_GetTileInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_gettileinfo.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetTileInfo, ListView_GetTileInfo macro [Windows Controls], _win32_ListView_GetTileInfo, _win32_ListView_GetTileInfo_cpp, commctrl/ListView_GetTileInfo, controls.ListView_GetTileInfo, controls._win32_ListView_GetTileInfo
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
 - ListView_GetTileInfo
 - commctrl/ListView_GetTileInfo
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
 - ListView_GetTileInfo
---

# ListView_GetTileInfo macro

## -syntax

```cpp
void ListView_GetTileInfo(
   HWND        hwnd,
   PLVTILEINFO pti
);
```


## -description

Gets information about a tile in a list-view control. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-gettileinfo">LVM_GETTILEINFO</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param pti

Type: <b>PLVTILEINFO</b>

<a href="/windows/desktop/api/commctrl/ns-commctrl-lvtileinfo">LVTILEINFO</a>

## -remarks

To use <b>ListView_GetTileInfo</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
