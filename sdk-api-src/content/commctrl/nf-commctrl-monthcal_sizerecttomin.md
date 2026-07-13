---
UID: NF:commctrl.MonthCal_SizeRectToMin
title: MonthCal_SizeRectToMin macro (commctrl.h)
description: Calculates how many calendars will fit in the given rectangle, and then returns the minimum size that a rectangle needs to be to fit that number of calendars. You can use this macro or send the MCM_SIZERECTTOMIN message explicitly.
helpviewer_keywords: ["MonthCal_SizeRectToMin","MonthCal_SizeRectToMin macro [Windows Controls]","_shell_MonthCal_SizeRectToMin","_shell_MonthCal_SizeRectToMin_cpp","commctrl/MonthCal_SizeRectToMin","controls.MonthCal_SizeRectToMin","controls._shell_MonthCal_SizeRectToMin"]
old-location: controls\MonthCal_SizeRectToMin.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_sizerecttomin.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_SizeRectToMin, MonthCal_SizeRectToMin macro [Windows Controls], _shell_MonthCal_SizeRectToMin, _shell_MonthCal_SizeRectToMin_cpp, commctrl/MonthCal_SizeRectToMin, controls.MonthCal_SizeRectToMin, controls._shell_MonthCal_SizeRectToMin
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
 - MonthCal_SizeRectToMin
 - commctrl/MonthCal_SizeRectToMin
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
 - MonthCal_SizeRectToMin
---

# MonthCal_SizeRectToMin macro

## -syntax

```cpp
LRESULT MonthCal_SizeRectToMin(
            HWND hmc,
  [in, out] RECT prc
);
```

## -returns

Type: **[LRESULT](/windows/desktop/winprog/windows-data-types)**

Unused.


## -description

Calculates how many calendars will fit in the given rectangle, and then returns the minimum size that a rectangle needs to be to fit that number of calendars. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-sizerecttomin">MCM_SIZERECTTOMIN</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.

### -param prc [in, out]

Type: <b><a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a></b>

On entry, contains a pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that describes a region that is greater than or equal to the size necessary to fit the desired number of calendars. When this function returns, contains the minimum <b>RECT</b> structure that fits this number of calendars.
