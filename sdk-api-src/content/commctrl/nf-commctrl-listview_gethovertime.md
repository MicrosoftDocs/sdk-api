---
UID: NF:commctrl.ListView_GetHoverTime
title: ListView_GetHoverTime macro (commctrl.h)
description: Gets the amount of time that the mouse cursor must hover over an item before it is selected. You can use this macro or send the LVM_GETHOVERTIME message explicitly.
helpviewer_keywords: ["ListView_GetHoverTime","ListView_GetHoverTime macro [Windows Controls]","_win32_ListView_GetHoverTime","_win32_ListView_GetHoverTime_cpp","commctrl/ListView_GetHoverTime","controls.ListView_GetHoverTime","controls._win32_ListView_GetHoverTime"]
old-location: controls\ListView_GetHoverTime.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_gethovertime.htm
ms.date: 12/05/2018
ms.keywords: ListView_GetHoverTime, ListView_GetHoverTime macro [Windows Controls], _win32_ListView_GetHoverTime, _win32_ListView_GetHoverTime_cpp, commctrl/ListView_GetHoverTime, controls.ListView_GetHoverTime, controls._win32_ListView_GetHoverTime
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
 - ListView_GetHoverTime
 - commctrl/ListView_GetHoverTime
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
 - ListView_GetHoverTime
---

# ListView_GetHoverTime macro


## -description

Gets the amount of time that the mouse cursor must hover over an item before it is selected. You can use this macro or send the <a href="/windows/desktop/Controls/lvm-gethovertime">LVM_GETHOVERTIME</a> message explicitly.

## -parameters

### -param hwndLV

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a list-view control.

## -remarks

The hover time only affects list-view controls that have the <a href="/windows/desktop/Controls/extended-list-view-styles">LVS_EX_TRACKSELECT</a>, <a href="/windows/desktop/Controls/extended-list-view-styles">LVS_EX_ONECLICKACTIVATE</a>, or <a href="/windows/desktop/Controls/extended-list-view-styles">LVS_EX_TWOCLICKACTIVATE</a> extended list-view style.