---
UID: NF:commctrl.MonthCal_GetCalendarBorder
title: MonthCal_GetCalendarBorder macro (commctrl.h)
description: Gets the border size, in pixels, of a month calendar control. You can use this macro or send the MCM_GETCALENDARBORDER message explicitly.
helpviewer_keywords: ["MonthCal_GetCalendarBorder","MonthCal_GetCalendarBorder macro [Windows Controls]","_shell_MonthCal_GetCalendarBorder","_shell_MonthCal_GetCalendarBorder_cpp","commctrl/MonthCal_GetCalendarBorder","controls.MonthCal_GetCalendarBorder","controls._shell_MonthCal_GetCalendarBorder"]
old-location: controls\MonthCal_GetCalendarBorder.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getcalendarborder.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_GetCalendarBorder, MonthCal_GetCalendarBorder macro [Windows Controls], _shell_MonthCal_GetCalendarBorder, _shell_MonthCal_GetCalendarBorder_cpp, commctrl/MonthCal_GetCalendarBorder, controls.MonthCal_GetCalendarBorder, controls._shell_MonthCal_GetCalendarBorder
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
 - MonthCal_GetCalendarBorder
 - commctrl/MonthCal_GetCalendarBorder
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
 - MonthCal_GetCalendarBorder
---

# MonthCal_GetCalendarBorder macro

## -syntax

```cpp
DWORD MonthCal_GetCalendarBorder(
   HWND hmc
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Current border size, in pixels.


## -description

Gets the border size, in pixels, of a month calendar control. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-getcalendarborder">MCM_GETCALENDARBORDER</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.
