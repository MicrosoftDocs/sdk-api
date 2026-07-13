---
UID: NF:commctrl.DateTime_GetRange
title: DateTime_GetRange macro (commctrl.h)
description: Gets the current minimum and maximum allowable system times for a date and time picker (DTP) control. You can use this macro, or send the DTM_GETRANGE message explicitly.
helpviewer_keywords: ["DateTime_GetRange","DateTime_GetRange macro [Windows Controls]","_win32_DateTime_GetRange","_win32_DateTime_GetRange_cpp","commctrl/DateTime_GetRange","controls.DateTime_GetRange","controls._win32_DateTime_GetRange"]
old-location: controls\DateTime_GetRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_getrange.htm
ms.date: 10/21/2024
ms.keywords: DateTime_GetRange, DateTime_GetRange macro [Windows Controls], _win32_DateTime_GetRange, _win32_DateTime_GetRange_cpp, commctrl/DateTime_GetRange, controls.DateTime_GetRange, controls._win32_DateTime_GetRange
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
 - DateTime_GetRange
 - commctrl/DateTime_GetRange
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
 - DateTime_GetRange
---

# DateTime_GetRange macro

## -syntax

```cpp
DWORD DateTime_GetRange(
   HWND         hdp,
   LPSYSTEMTIME rgst
);
```

## -returns

Type: **[DWORD](/windows/desktop/winprog/windows-data-types)**

Returns a <b>DWORD</b> value that is a combination of GDTR_MIN or GDTR_MAX. The first element of the <b>SYSTEMTIME</b> array contains the minimum allowable time. The second element of the <b>SYSTEMTIME</b> array contains the maximum allowable time.


## -description

Gets the current minimum and maximum allowable system times for a date and time picker (DTP) control. You can use this macro, or send the <a href="/windows/desktop/Controls/dtm-getrange">DTM_GETRANGE</a> message explicitly.

## -parameters

### -param hdp

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a DTP control.

### -param rgst

Type: <b>LPSYSTEMTIME</b>

A pointer to a two-element array of <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structures.

## -remarks

The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range. If the <a href="/windows/desktop/api/commctrl/nf-commctrl-datetime_setsystemtime">DateTime_SetSystemtime</a> message specifies a date and time that falls outside the range, it will fail.
