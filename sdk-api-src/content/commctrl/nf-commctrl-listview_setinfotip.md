---
UID: NF:commctrl.ListView_SetInfoTip
title: ListView_SetInfoTip macro (commctrl.h)
description: Sets tooltip text. You can use this macro or send the LVM_SETINFOTIP message explicitly.
helpviewer_keywords: ["ListView_SetInfoTip","ListView_SetInfoTip macro [Windows Controls]","_win32_ListView_SetInfoTip","_win32_ListView_SetInfoTip_cpp","commctrl/ListView_SetInfoTip","controls.ListView_SetInfoTip","controls._win32_ListView_SetInfoTip"]
old-location: controls\ListView_SetInfoTip.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setinfotip.htm
ms.date: 10/21/2024
ms.keywords: ListView_SetInfoTip, ListView_SetInfoTip macro [Windows Controls], _win32_ListView_SetInfoTip, _win32_ListView_SetInfoTip_cpp, commctrl/ListView_SetInfoTip, controls.ListView_SetInfoTip, controls._win32_ListView_SetInfoTip
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
 - ListView_SetInfoTip
 - commctrl/ListView_SetInfoTip
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
 - ListView_SetInfoTip
---

# ListView_SetInfoTip macro

## -syntax

```cpp
BOOL ListView_SetInfoTip(
   HWND          hwndLV,
   PLVSETINFOTIP plvInfoTip
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if the tooltip text is set successfully, or <b>FALSE</b> otherwise.


## -description

Sets tooltip text. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-setinfotip">LVM_SETINFOTIP</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param plvInfoTip

Type: <b>PLVSETINFOTIP</b>

<a href="/windows/desktop/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a>

## -remarks

To use <b>ListView_SetInfoTip</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
