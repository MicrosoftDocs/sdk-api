---
UID: NF:commctrl.MonthCal_GetCurrentView
title: MonthCal_GetCurrentView macro (commctrl.h)
description: Gets the view for a month calendar control. You can use this macro or send the MCM_GETCURRENTVIEW message explicitly.
helpviewer_keywords: ["MonthCal_GetCurrentView","MonthCal_GetCurrentView macro [Windows Controls]","_shell_MonthCal_GetCurrentView","_shell_MonthCal_GetCurrentView_cpp","commctrl/MonthCal_GetCurrentView","controls.MonthCal_GetCurrentView","controls._shell_MonthCal_GetCurrentView"]
old-location: controls\MonthCal_GetCurrentView.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getcurrentview.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_GetCurrentView, MonthCal_GetCurrentView macro [Windows Controls], _shell_MonthCal_GetCurrentView, _shell_MonthCal_GetCurrentView_cpp, commctrl/MonthCal_GetCurrentView, controls.MonthCal_GetCurrentView, controls._shell_MonthCal_GetCurrentView
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
 - MonthCal_GetCurrentView
 - commctrl/MonthCal_GetCurrentView
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
 - MonthCal_GetCurrentView
---

# MonthCal_GetCurrentView macro

## -syntax

```cpp
DWORD MonthCal_GetCurrentView(
   HWND hmc
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Current view. One of the following values.

| Return code | Description |
|---|---|
| MCMV_MONTH | Monthly view. |
| MCMV_YEAR | Annual view. |
| MCMV_DECADE | Decade view. |
| MCMV_CENTURY | Century view. |

## -description

Gets the view for a month calendar control. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-getcurrentview">MCM_GETCURRENTVIEW</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.
