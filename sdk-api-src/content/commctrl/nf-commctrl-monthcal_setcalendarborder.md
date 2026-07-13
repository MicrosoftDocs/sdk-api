---
UID: NF:commctrl.MonthCal_SetCalendarBorder
title: MonthCal_SetCalendarBorder macro (commctrl.h)
description: Sets the border size, in pixels, of a month calendar control. You can use this macro or send the MCM_SETCALENDARBORDER message explicitly.
helpviewer_keywords: ["MonthCal_SetCalendarBorder","MonthCal_SetCalendarBorder macro [Windows Controls]","_shell_MonthCal_SetCalendarBorder","_shell_MonthCal_SetCalendarBorder_cpp","commctrl/MonthCal_SetCalendarBorder","controls.MonthCal_SetCalendarBorder","controls._shell_MonthCal_SetCalendarBorder"]
old-location: controls\MonthCal_SetCalendarBorder.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setcalendarborder.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_SetCalendarBorder, MonthCal_SetCalendarBorder macro [Windows Controls], _shell_MonthCal_SetCalendarBorder, _shell_MonthCal_SetCalendarBorder_cpp, commctrl/MonthCal_SetCalendarBorder, controls.MonthCal_SetCalendarBorder, controls._shell_MonthCal_SetCalendarBorder
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
 - MonthCal_SetCalendarBorder
 - commctrl/MonthCal_SetCalendarBorder
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
 - MonthCal_SetCalendarBorder
---

# MonthCal_SetCalendarBorder macro

## -syntax

```cpp
LRESULT MonthCal_SetCalendarBorder(
   HWND hmc,
   BOOL fset,
   int  xyborder
);
```

## -returns

Type: **[LRESULT](/windows/desktop/winprog/windows-data-types)**

Unused.


## -description

Sets the border size, in pixels, of a month calendar control. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-setcalendarborder">MCM_SETCALENDARBORDER</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.

### -param fset

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

If <b>TRUE</b>, then the border size is set to the number of pixels that <i>xyborder</i> specifies. If <b>FALSE</b>, then the border size is reset to the default value specified by the theme, or zero if themes are not being used.

### -param xyborder

Type: <b>int</b>

Number of pixels of the border size.
