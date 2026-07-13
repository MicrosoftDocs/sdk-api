---
UID: NF:commctrl.ListView_IsGroupViewEnabled
title: ListView_IsGroupViewEnabled macro (commctrl.h)
description: Checks whether the list-view control has group view enabled. You can use this macro or send the LVM_ISGROUPVIEWENABLED message explicitly.
helpviewer_keywords: ["ListView_IsGroupViewEnabled","ListView_IsGroupViewEnabled macro [Windows Controls]","_win32_ListView_IsGroupViewEnabled","_win32_ListView_IsGroupViewEnabled_cpp","commctrl/ListView_IsGroupViewEnabled","controls.ListView_IsGroupViewEnabled","controls._win32_ListView_IsGroupViewEnabled"]
old-location: controls\ListView_IsGroupViewEnabled.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_isgroupviewenabled.htm
ms.date: 10/21/2024
ms.keywords: ListView_IsGroupViewEnabled, ListView_IsGroupViewEnabled macro [Windows Controls], _win32_ListView_IsGroupViewEnabled, _win32_ListView_IsGroupViewEnabled_cpp, commctrl/ListView_IsGroupViewEnabled, controls.ListView_IsGroupViewEnabled, controls._win32_ListView_IsGroupViewEnabled
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
 - ListView_IsGroupViewEnabled
 - commctrl/ListView_IsGroupViewEnabled
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
 - ListView_IsGroupViewEnabled
---

# ListView_IsGroupViewEnabled macro

## -syntax

```cpp
BOOL ListView_IsGroupViewEnabled(
   HWND hwnd
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns <b>TRUE</b> if group view is enabled, or <b>FALSE</b> otherwise.


## -description

Checks whether the list-view control has group view
 enabled. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-isgroupviewenabled">LVM_ISGROUPVIEWENABLED</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

## -remarks

To use <b>ListView_IsGroupViewEnabled</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
