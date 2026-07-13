---
UID: NF:commctrl.MonthCal_GetCalendarCount
title: MonthCal_GetCalendarCount macro (commctrl.h)
description: Gets the number of calendars currently displayed in the calendar control. You can use this macro or send the MCM_GETCALENDARCOUNT message explicitly.
helpviewer_keywords: ["MonthCal_GetCalendarCount","MonthCal_GetCalendarCount macro [Windows Controls]","_shell_MonthCal_GetCalendarCount","_shell_MonthCal_GetCalendarCount_cpp","commctrl/MonthCal_GetCalendarCount","controls.MonthCal_GetCalendarCount","controls._shell_MonthCal_GetCalendarCount"]
old-location: controls\MonthCal_GetCalendarCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getcalendarcount.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_GetCalendarCount, MonthCal_GetCalendarCount macro [Windows Controls], _shell_MonthCal_GetCalendarCount, _shell_MonthCal_GetCalendarCount_cpp, commctrl/MonthCal_GetCalendarCount, controls.MonthCal_GetCalendarCount, controls._shell_MonthCal_GetCalendarCount
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - MonthCal_GetCalendarCount
 - commctrl/MonthCal_GetCalendarCount
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
 - MonthCal_GetCalendarCount
---

# MonthCal_GetCalendarCount macro

## -syntax

```cpp
DWORD MonthCal_GetCalendarCount(
   HWND hmc
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Number of calendars currently displayed in the calendar control. The maximum number of allowed calendars is 12.


## -description

Gets the number of calendars currently displayed in the calendar control. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-getcalendarcount">MCM_GETCALENDARCOUNT</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.
