---
UID: NF:commctrl.MonthCal_SetToday
title: MonthCal_SetToday macro (commctrl.h)
description: Sets the &quot;today&quot; selection for a month calendar control. You can use this macro or send the MCM_SETTODAY message explicitly.
helpviewer_keywords: ["MonthCal_SetToday","MonthCal_SetToday macro [Windows Controls]","_win32_MonthCal_SetToday","_win32_MonthCal_SetToday_cpp","commctrl/MonthCal_SetToday","controls.MonthCal_SetToday","controls._win32_MonthCal_SetToday"]
old-location: controls\MonthCal_SetToday.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_settoday.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_SetToday, MonthCal_SetToday macro [Windows Controls], _win32_MonthCal_SetToday, _win32_MonthCal_SetToday_cpp, commctrl/MonthCal_SetToday, controls.MonthCal_SetToday, controls._win32_MonthCal_SetToday
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
 - MonthCal_SetToday
 - commctrl/MonthCal_SetToday
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
 - MonthCal_SetToday
---

# MonthCal_SetToday macro

## -syntax

```cpp
void MonthCal_SetToday(
   HWND         hmc,
   LPSYSTEMTIME pst
);
```


## -description

Sets the "today" selection for a month calendar control. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-settoday">MCM_SETTODAY</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.

### -param pst

Type: <b>LPSYSTEMTIME</b>

Pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the date to be set as the "today" selection for the control. If this parameter is set to <b>NULL</b>, the control returns to the default setting. The time members of this structure are ignored. If the "today" selection is set to any date other than the default, the following conditions apply:
 

<ul>
<li>The control will not automatically update the "today" selection when the time passes midnight for the current day.</li>
<li>The control will not automatically update its display based on locale changes.</li>
</ul>
