---
UID: NF:commctrl.ListView_SetGroupMetrics
title: ListView_SetGroupMetrics macro (commctrl.h)
description: Sets information about the display of groups. You can use this macro or send the LVM_SETGROUPMETRICS message explicitly.helpviewer_keywords: ["ListView_SetGroupMetrics","ListView_SetGroupMetrics macro [Windows Controls]","_win32_ListView_SetGroupMetrics","_win32_ListView_SetGroupMetrics_cpp","commctrl/ListView_SetGroupMetrics","controls.ListView_SetGroupMetrics","controls._win32_ListView_SetGroupMetrics"]
old-location: controls\ListView_SetGroupMetrics.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setgroupmetrics.htm
ms.date: 12/05/2018
ms.keywords: ListView_SetGroupMetrics, ListView_SetGroupMetrics macro [Windows Controls], _win32_ListView_SetGroupMetrics, _win32_ListView_SetGroupMetrics_cpp, commctrl/ListView_SetGroupMetrics, controls.ListView_SetGroupMetrics, controls._win32_ListView_SetGroupMetrics
f1_keywords:
- commctrl/ListView_SetGroupMetrics
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Commctrl.h
api_name:
- ListView_SetGroupMetrics
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_SetGroupMetrics macro


## -description


Sets information about the display of groups. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-setgroupmetrics">LVM_SETGROUPMETRICS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


### -param pGroupMetrics

Type: <b>PLVGROUPMETRICS</b>

<a href="https://docs.microsoft.com/windows/desktop/api/commctrl/ns-commctrl-lvgroupmetrics">LVGROUPMETRICS</a>

## -remarks



To use <b>ListView_SetGroupMetrics</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://docs.microsoft.com/windows/desktop/Controls/cookbook-overview">Enabling Visual Styles</a>. 



