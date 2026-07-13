---
UID: NF:commctrl.MonthCal_GetCALID
title: MonthCal_GetCALID macro (commctrl.h)
description: Gets the current calendar ID for the given calendar control. You can use this macro or send the MCM_GETCALID message explicitly.
helpviewer_keywords: ["MonthCal_GetCALID","MonthCal_GetCALID macro [Windows Controls]","_shell_MonthCal_GetCALID","_shell_MonthCal_GetCALID_cpp","commctrl/MonthCal_GetCALID","controls.MonthCal_GetCALID","controls._shell_MonthCal_GetCALID"]
old-location: controls\MonthCal_GetCALID.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getcalid.htm
ms.date: 10/21/2024
ms.keywords: MonthCal_GetCALID, MonthCal_GetCALID macro [Windows Controls], _shell_MonthCal_GetCALID, _shell_MonthCal_GetCALID_cpp, commctrl/MonthCal_GetCALID, controls.MonthCal_GetCALID, controls._shell_MonthCal_GetCALID
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
 - MonthCal_GetCALID
 - commctrl/MonthCal_GetCALID
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
 - MonthCal_GetCALID
---

# MonthCal_GetCALID macro

## -syntax

```cpp
CALID MonthCal_GetCALID(
   HWND hmc
);
```

## -returns

Type: **CALID**

ID of the current calendar. One of the Calendar Identifiers constants.


## -description

Gets the current calendar ID for the given calendar control. You can use this macro or send the <a href="/windows/desktop/Controls/mcm-getcalid">MCM_GETCALID</a> message explicitly.

## -parameters

### -param hmc

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control.
