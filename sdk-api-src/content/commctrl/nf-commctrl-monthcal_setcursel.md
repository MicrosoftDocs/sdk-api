---
UID: NF:commctrl.MonthCal_SetCurSel
title: MonthCal_SetCurSel macro (commctrl.h)
description: Sets the currently selected date for a month calendar control. If the specified date is not in view, the control updates the display to bring it into view. You can use this macro or send the MCM_SETCURSEL message explicitly.
helpviewer_keywords: ["MonthCal_SetCurSel","MonthCal_SetCurSel macro [Windows Controls]","_win32_MonthCal_SetCurSel","_win32_MonthCal_SetCurSel_cpp","commctrl/MonthCal_SetCurSel","controls.MonthCal_SetCurSel","controls._win32_MonthCal_SetCurSel"]
old-location: controls\MonthCal_SetCurSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setcursel.htm
ms.date: 12/05/2018
ms.keywords: MonthCal_SetCurSel, MonthCal_SetCurSel macro [Windows Controls], _win32_MonthCal_SetCurSel, _win32_MonthCal_SetCurSel_cpp, commctrl/MonthCal_SetCurSel, controls.MonthCal_SetCurSel, controls._win32_MonthCal_SetCurSel
f1_keywords:
- commctrl/MonthCal_SetCurSel
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
- MonthCal_SetCurSel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MonthCal_SetCurSel macro


## -description


Sets the currently selected date for a month calendar control. If the specified date is not in view, the control updates the display to bring it into view. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/mcm-setcursel">MCM_SETCURSEL</a> message explicitly. 


## -parameters




### -param hmc

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control. 


### -param pst

Type: <b>LPSYSTEMTIME</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the date to be set as the current selection. The time members of this structure are ignored. 

