---
UID: NF:commctrl.MonthCal_SetCALID
title: MonthCal_SetCALID macro (commctrl.h)
description: Sets the calendar ID for the given calendar control. You can use this macro or send the MCM_SETCALID message explicitly.
helpviewer_keywords: ["MonthCal_SetCALID","MonthCal_SetCALID macro [Windows Controls]","_shell_MonthCal_SetCALID","_shell_MonthCal_SetCALID_cpp","commctrl/MonthCal_SetCALID","controls.MonthCal_SetCALID","controls._shell_MonthCal_SetCALID"]
old-location: controls\MonthCal_SetCALID.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setcalid.htm
ms.date: 12/05/2018
ms.keywords: MonthCal_SetCALID, MonthCal_SetCALID macro [Windows Controls], _shell_MonthCal_SetCALID, _shell_MonthCal_SetCALID_cpp, commctrl/MonthCal_SetCALID, controls.MonthCal_SetCALID, controls._shell_MonthCal_SetCALID
f1_keywords:
- commctrl/MonthCal_SetCALID
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Commctrl.h
api_name:
- MonthCal_SetCALID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MonthCal_SetCALID macro


## -description


Sets the calendar ID for the given calendar control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/mcm-setcalid">MCM_SETCALID</a> message explicitly.


## -parameters




### -param hmc

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.


### -param calid

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Calendar ID. One of the <a href="https://docs.microsoft.com/windows/desktop/Intl/calendar-identifiers">Calendar Identifiers</a> constants.

