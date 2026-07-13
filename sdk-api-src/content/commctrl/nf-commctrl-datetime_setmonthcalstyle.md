---
UID: NF:commctrl.DateTime_SetMonthCalStyle
title: DateTime_SetMonthCalStyle macro (commctrl.h)
description: Sets the style for a specified date and time picker (DTP) control. Use this macro or send the DTM_SETMCSTYLE message explicitly.
helpviewer_keywords: ["DateTime_SetMonthCalStyle","DateTime_SetMonthCalStyle macro [Windows Controls]","_shell_DateTime_SetMonthCalStyle","_shell_DateTime_SetMonthCalStyle_cpp","commctrl/DateTime_SetMonthCalStyle","controls.DateTime_SetMonthCalStyle","controls._shell_DateTime_SetMonthCalStyle"]
old-location: controls\DateTime_SetMonthCalStyle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_setmonthcalstyle.htm
ms.date: 10/21/2024
ms.keywords: DateTime_SetMonthCalStyle, DateTime_SetMonthCalStyle macro [Windows Controls], _shell_DateTime_SetMonthCalStyle, _shell_DateTime_SetMonthCalStyle_cpp, commctrl/DateTime_SetMonthCalStyle, controls.DateTime_SetMonthCalStyle, controls._shell_DateTime_SetMonthCalStyle
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
 - DateTime_SetMonthCalStyle
 - commctrl/DateTime_SetMonthCalStyle
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
 - DateTime_SetMonthCalStyle
---

# DateTime_SetMonthCalStyle macro

## -syntax

```cpp
LRESULT DateTime_SetMonthCalStyle(
  [in] HWND  hdp,
  [in] DWORD dwStyle
);
```

## -returns

Type: **[LRESULT](/windows/desktop/winprog/windows-data-types)**

Returns the value of the previous style.


## -description

Sets the style for a specified date and time picker (DTP) control. Use this macro or send the <a href="/windows/desktop/Controls/dtm-setmcstyle">DTM_SETMCSTYLE</a> message explicitly.

## -parameters

### -param hdp [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the DTP.

### -param dwStyle [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

<a href="/windows/desktop/Controls/month-calendar-control-styles">Month Calendar Control Styles</a>
