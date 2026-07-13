---
UID: NF:commctrl.ListView_GetGroupMetrics
title: ListView_GetGroupMetrics macro (commctrl.h)
description: Gets information about the display of groups. You can use this macro or send the LVM_GETGROUPMETRICS message explicitly.
helpviewer_keywords: ["ListView_GetGroupMetrics","ListView_GetGroupMetrics macro [Windows Controls]","_win32_ListView_GetGroupMetrics","_win32_ListView_GetGroupMetrics_cpp","commctrl/ListView_GetGroupMetrics","controls.ListView_GetGroupMetrics","controls._win32_ListView_GetGroupMetrics"]
old-location: controls\ListView_GetGroupMetrics.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getgroupmetrics.htm
ms.date: 10/21/2024
ms.keywords: ListView_GetGroupMetrics, ListView_GetGroupMetrics macro [Windows Controls], _win32_ListView_GetGroupMetrics, _win32_ListView_GetGroupMetrics_cpp, commctrl/ListView_GetGroupMetrics, controls.ListView_GetGroupMetrics, controls._win32_ListView_GetGroupMetrics
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
 - ListView_GetGroupMetrics
 - commctrl/ListView_GetGroupMetrics
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
 - ListView_GetGroupMetrics
---

# ListView_GetGroupMetrics macro

## -syntax

```cpp
void ListView_GetGroupMetrics(
   HWND            hwnd,
   PLVGROUPMETRICS pGroupMetrics
);
```


## -description

Gets information about the display of groups. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-getgroupmetrics">LVM_GETGROUPMETRICS</a> message explicitly.

## -parameters

### -param hwnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control.

### -param pGroupMetrics

Type: <b>PLVGROUPMETRICS</b>

<a href="/windows/desktop/api/commctrl/ns-commctrl-lvgroupmetrics">LVGROUPMETRICS</a>

## -remarks

To use <b>ListView_GetGroupMetrics</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>.
