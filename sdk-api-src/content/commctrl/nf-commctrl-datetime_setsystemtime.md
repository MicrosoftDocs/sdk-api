---
UID: NF:commctrl.DateTime_SetSystemtime
title: DateTime_SetSystemtime macro (commctrl.h)
description: Sets a date and time picker (DTP) control to a given date and time. You can use this macro or send the DTM_SETSYSTEMTIME message explicitly.
helpviewer_keywords: ["DateTime_SetSystemtime","DateTime_SetSystemtime macro [Windows Controls]","GDT_NONE","GDT_VALID","_win32_DateTime_SetSystemtime","_win32_DateTime_SetSystemtime_cpp","commctrl/DateTime_SetSystemtime","controls.DateTime_SetSystemtime","controls._win32_DateTime_SetSystemtime"]
old-location: controls\DateTime_SetSystemtime.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_setsystemtime.htm
ms.date: 10/21/2024
ms.keywords: DateTime_SetSystemtime, DateTime_SetSystemtime macro [Windows Controls], GDT_NONE, GDT_VALID, _win32_DateTime_SetSystemtime, _win32_DateTime_SetSystemtime_cpp, commctrl/DateTime_SetSystemtime, controls.DateTime_SetSystemtime, controls._win32_DateTime_SetSystemtime
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
 - DateTime_SetSystemtime
 - commctrl/DateTime_SetSystemtime
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
 - DateTime_SetSystemtime
---

# DateTime_SetSystemtime macro

## -syntax

```cpp
BOOL DateTime_SetSystemtime(
   HWND         hdp,
   DWORD        gd,
   LPSYSTEMTIME pst
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns nonzero if successful, or zero otherwise.


## -description

Sets a date and time picker (DTP) control to a given date and time. You can use this macro or send the <a href="/windows/desktop/Controls/dtm-setsystemtime">DTM_SETSYSTEMTIME</a> message explicitly.

## -parameters

### -param hdp

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a DTP control.

### -param gd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A value that specifies the action that should be performed. This should be set to one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GDT_VALID"></a><a id="gdt_valid"></a><dl>
<dt><b>GDT_VALID</b></dt>
</dl>
</td>
<td width="60%">
Set the DTP control according to the data within the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure pointed to by <i>pst</i>. 

</td>
</tr>
<tr>
<td width="40%"><a id="GDT_NONE"></a><a id="gdt_none"></a><dl>
<dt><b>GDT_NONE</b></dt>
</dl>
</td>
<td width="60%">
Set the DTP control to "no date" and clear its check box. When this flag is specified, <i>pst</i> is ignored. This flag applies only to DTP controls that are set to the <a href="/windows/desktop/Controls/date-and-time-picker-control-styles">DTS_SHOWNONE</a> style.

</td>
</tr>
</table>

### -param pst

Type: <b>LPSYSTEMTIME</b>

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the system time information by which to set the DTP control.
