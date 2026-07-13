---
UID: NF:commctrl.ListView_GetTileViewInfo
title: ListView_GetTileViewInfo macro (commctrl.h)
description: Gets information about a list-view control in tile view. You can use this macro or send the LVM_GETTILEVIEWINFO message explicitly.
helpviewer_keywords: ["ListView_GetTileViewInfo","ListView_GetTileViewInfo macro [Windows Controls]","_win32_ListView_GetTileViewInfo","_win32_ListView_GetTileViewInfo_cpp","commctrl/ListView_GetTileViewInfo","controls.ListView_GetTileViewInfo","controls._win32_ListView_GetTileViewInfo"]
old-location: controls\ListView_GetTileViewInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_gettileviewinfo.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetTileViewInfo, ListView_GetTileViewInfo macro [Windows Controls], _win32_ListView_GetTileViewInfo, _win32_ListView_GetTileViewInfo_cpp, commctrl/ListView_GetTileViewInfo, controls.ListView_GetTileViewInfo, controls._win32_ListView_GetTileViewInfo
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
 - ListView_GetTileViewInfo
 - commctrl/ListView_GetTileViewInfo
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
 - ListView_GetTileViewInfo
---

# ListView_GetTileViewInfo macro

## -syntax

```cpp
void ListView_GetTileViewInfo(
   HWND            hwnd,
   PLVTILEVIEWINFO ptvi
);
```


## -description

Gets information about a list-view control in tile view. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-gettileviewinfo">LVM_GETTILEVIEWINFO</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param ptvi

Type: <b>PLVTILEVIEWINFO</b>

<a href="/windows/desktop/api/commctrl/ns-commctrl-lvtileviewinfo">LVTILEVIEWINFO</a>

## -remarks

To use <b>ListView_GetTileViewInfo</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
