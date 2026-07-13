---
UID: NF:commctrl.DateTime_SetRange
title: DateTime_SetRange macro (commctrl.h)
description: Sets the minimum and maximum allowable system times for a date and time picker (DTP) control. You can use this macro or send the DTM_SETRANGE message explicitly.
helpviewer_keywords: ["DateTime_SetRange","DateTime_SetRange macro [Windows Controls]","GDTR_MAX","GDTR_MIN","_win32_DateTime_SetRange","_win32_DateTime_SetRange_cpp","commctrl/DateTime_SetRange","controls.DateTime_SetRange","controls._win32_DateTime_SetRange"]
old-location: controls\DateTime_SetRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_setrange.htm
ms.date: 10/21/2024
ms.keywords: DateTime_SetRange, DateTime_SetRange macro [Windows Controls], GDTR_MAX, GDTR_MIN, _win32_DateTime_SetRange, _win32_DateTime_SetRange_cpp, commctrl/DateTime_SetRange, controls.DateTime_SetRange, controls._win32_DateTime_SetRange
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
 - DateTime_SetRange
 - commctrl/DateTime_SetRange
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
 - DateTime_SetRange
---

# DateTime_SetRange macro

## -syntax

```cpp
BOOL DateTime_SetRange(
   HWND         hdp,
   DWORD        gd,
   LPSYSTEMTIME rgst
);
```

## -returns

Type: **[BOOL](/windows/desktop/winprog/windows-data-types)**

Returns nonzero if successful, or zero otherwise.


## -description

Sets the minimum and maximum allowable system times for a date and time picker (DTP) control. You can use this macro or send the <a href="/windows/desktop/Controls/dtm-setrange">DTM_SETRANGE</a> message explicitly.

## -parameters

### -param hdp

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a DTP control.

### -param gd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

A value that specifies which range values are valid. This value can be a combination of the following: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GDTR_MIN"></a><a id="gdtr_min"></a><dl>
<dt><b>GDTR_MIN</b></dt>
</dl>
</td>
<td width="60%">
The first element in the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure array is valid and will be used to set the minimum allowable system time.

</td>
</tr>
<tr>
<td width="40%"><a id="GDTR_MAX"></a><a id="gdtr_max"></a><dl>
<dt><b>GDTR_MAX</b></dt>
</dl>
</td>
<td width="60%">
The second element in the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure array is valid and will be used to set the maximum allowable system time.

</td>
</tr>
</table>

### -param rgst

Type: <b>LPSYSTEMTIME</b>

A pointer to a two-element array of <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structures. The first element of the <b>SYSTEMTIME</b> array contains the minimum allowable time. The second element of the <b>SYSTEMTIME</b> array contains the maximum allowable time. It is not necessary to fill an array element that is not specified in the <i>gd</i> parameter.

## -remarks

The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range. If the <a href="/windows/desktop/api/commctrl/nf-commctrl-datetime_setsystemtime">DateTime_SetSystemtime</a> message specifies a date and time that falls outside the range, it will fail.
