---
UID: NF:commctrl.DateTime_SetFormat
title: DateTime_SetFormat macro (commctrl.h)
description: Sets the display of a date and time picker (DTP) control based on a given format string. You can use this macro or send the DTM_SETFORMAT message explicitly.
helpviewer_keywords: ["DateTime_SetFormat","DateTime_SetFormat macro [Windows Controls]","_win32_DateTime_SetFormat","_win32_DateTime_SetFormat_cpp","commctrl/DateTime_SetFormat","controls.DateTime_SetFormat","controls._win32_DateTime_SetFormat"]
old-location: controls\DateTime_SetFormat.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_setformat.htm
ms.date: 10/21/2024
ms.keywords: DateTime_SetFormat, DateTime_SetFormat macro [Windows Controls], _win32_DateTime_SetFormat, _win32_DateTime_SetFormat_cpp, commctrl/DateTime_SetFormat, controls.DateTime_SetFormat, controls._win32_DateTime_SetFormat
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
 - DateTime_SetFormat
 - commctrl/DateTime_SetFormat
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
 - DateTime_SetFormat
---

# DateTime_SetFormat macro

## -syntax

```cpp
void DateTime_SetFormat(
   HWND    hdp,
   LPCTSTR sz
);
```


## -description

Sets the display of a date and time picker (DTP) control based on a given format string. You can use this macro or send the <a href="/windows/desktop/Controls/dtm-setformat">DTM_SETFORMAT</a> message explicitly.

## -parameters

### -param hdp

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a DTP control.

### -param sz

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCTSTR</a></b>

A pointer to a zero-terminated <a href="/windows/desktop/Controls/date-and-time-picker-controls">format string</a> that defines the desired display. Setting this parameter to <b>NULL</b> will reset the control to the default format string for the current style.

## -remarks

It is acceptable to include extra characters within the format string to produce a more rich display. However, any nonformat characters must be enclosed within single quotes. For example, the format string "'Today is: 'hh':'m':'s ddddMMMdd', 'yyy" would produce output like "Today is: 04:22:31 Tuesday Mar 23, 1996". 

<div class="alert"><b>Note</b>   A DTP control tracks locale changes when it is using the default format string. If you set a custom format string, it will not be updated in response to locale changes.</div>
<div> </div>
