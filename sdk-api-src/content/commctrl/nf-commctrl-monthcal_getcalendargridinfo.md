---
UID: NF:commctrl.MonthCal_GetCalendarGridInfo
title: MonthCal_GetCalendarGridInfo macro (commctrl.h)
description: Gets information about a calendar grid.
helpviewer_keywords: ["MonthCal_GetCalendarGridInfo","MonthCal_GetCalendarGridInfo macro [Windows Controls]","_shell_MonthCal_GetCalendarGridInfo","_shell_MonthCal_GetCalendarGridInfo_cpp","commctrl/MonthCal_GetCalendarGridInfo","controls.MonthCal_GetCalendarGridInfo","controls._shell_MonthCal_GetCalendarGridInfo"]
old-location: controls\MonthCal_GetCalendarGridInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getcalendargridinfo.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_GetCalendarGridInfo, MonthCal_GetCalendarGridInfo macro [Windows Controls], _shell_MonthCal_GetCalendarGridInfo, _shell_MonthCal_GetCalendarGridInfo_cpp, commctrl/MonthCal_GetCalendarGridInfo, controls.MonthCal_GetCalendarGridInfo, controls._shell_MonthCal_GetCalendarGridInfo
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
 - MonthCal_GetCalendarGridInfo
 - commctrl/MonthCal_GetCalendarGridInfo
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
 - MonthCal_GetCalendarGridInfo
---

# MonthCal_GetCalendarGridInfo macro

## -syntax

```cpp
BOOL MonthCal_GetCalendarGridInfo(
   HWND       hmc,
   MCGRIDINFO *pmcGridInfo
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

<b>TRUE</b> if successful, otherwise <b>FALSE</b>.


## -description

Gets information about a calendar grid.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.

### -param pmcGridInfo

Type: <b><a href="/windows/desktop/api/commctrl/ns-commctrl-mcgridinfo">MCGRIDINFO</a>*</b>

Pointer to an <a href="/windows/desktop/api/commctrl/ns-commctrl-mcgridinfo">MCGRIDINFO</a> structure that contains information about the calendar grid.
