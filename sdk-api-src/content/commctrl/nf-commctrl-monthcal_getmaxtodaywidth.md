---
UID: NF:commctrl.MonthCal_GetMaxTodayWidth
title: MonthCal_GetMaxTodayWidth macro (commctrl.h)
description: Retrieves the maximum width of the &quot;today&quot; string in a month calendar control. This includes the label text and the date text. You can use this macro or send the MCM_GETMAXTODAYWIDTH message explicitly.
helpviewer_keywords: ["MonthCal_GetMaxTodayWidth","MonthCal_GetMaxTodayWidth macro [Windows Controls]","_win32_MonthCal_GetMaxTodayWidth","_win32_MonthCal_GetMaxTodayWidth_cpp","commctrl/MonthCal_GetMaxTodayWidth","controls.MonthCal_GetMaxTodayWidth","controls._win32_MonthCal_GetMaxTodayWidth"]
old-location: controls\MonthCal_GetMaxTodayWidth.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getmaxtodaywidth.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_GetMaxTodayWidth, MonthCal_GetMaxTodayWidth macro [Windows Controls], _win32_MonthCal_GetMaxTodayWidth, _win32_MonthCal_GetMaxTodayWidth_cpp, commctrl/MonthCal_GetMaxTodayWidth, controls.MonthCal_GetMaxTodayWidth, controls._win32_MonthCal_GetMaxTodayWidth
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
 - MonthCal_GetMaxTodayWidth
 - commctrl/MonthCal_GetMaxTodayWidth
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
 - MonthCal_GetMaxTodayWidth
---

# MonthCal_GetMaxTodayWidth macro

## -syntax

```cpp
DWORD MonthCal_GetMaxTodayWidth(
   HWND hmc
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns the width of the "today" string, in pixels.


## -description

Retrieves the maximum width of the "today" string in a month calendar control. This includes the label text and the date text. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-getmaxtodaywidth">MCM_GETMAXTODAYWIDTH</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.
