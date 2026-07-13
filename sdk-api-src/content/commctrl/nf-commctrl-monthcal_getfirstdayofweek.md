---
UID: NF:commctrl.MonthCal_GetFirstDayOfWeek
title: MonthCal_GetFirstDayOfWeek macro (commctrl.h)
description: Retrieves the first day of the week for a month calendar control. You can use this macro or send the MCM_GETFIRSTDAYOFWEEK message explicitly.
helpviewer_keywords: ["MonthCal_GetFirstDayOfWeek","MonthCal_GetFirstDayOfWeek macro [Windows Controls]","_win32_MonthCal_GetFirstDayOfWeek","_win32_MonthCal_GetFirstDayOfWeek_cpp","commctrl/MonthCal_GetFirstDayOfWeek","controls.MonthCal_GetFirstDayOfWeek","controls._win32_MonthCal_GetFirstDayOfWeek"]
old-location: controls\MonthCal_GetFirstDayOfWeek.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getfirstdayofweek.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_GetFirstDayOfWeek, MonthCal_GetFirstDayOfWeek macro [Windows Controls], _win32_MonthCal_GetFirstDayOfWeek, _win32_MonthCal_GetFirstDayOfWeek_cpp, commctrl/MonthCal_GetFirstDayOfWeek, controls.MonthCal_GetFirstDayOfWeek, controls._win32_MonthCal_GetFirstDayOfWeek
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
 - MonthCal_GetFirstDayOfWeek
 - commctrl/MonthCal_GetFirstDayOfWeek
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
 - MonthCal_GetFirstDayOfWeek
---

# MonthCal_GetFirstDayOfWeek macro

## -syntax

```cpp
DWORD MonthCal_GetFirstDayOfWeek(
   HWND hmc
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns a <b>DWORD</b> value that contains two values. The high word is a <b>BOOL</b> value that is nonzero if the first day of the week is set to something other than LOCALE_IFIRSTDAYOFWEEK, or zero otherwise. The low word is an INT value that represents the first day of the week, where 0 is Monday, 1 is Tuesday, and so on.


## -description

Retrieves the first day of the week for a month calendar control. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-getfirstdayofweek">MCM_GETFIRSTDAYOFWEEK</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.
