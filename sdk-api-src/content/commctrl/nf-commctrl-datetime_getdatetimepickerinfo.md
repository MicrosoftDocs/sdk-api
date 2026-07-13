---
UID: NF:commctrl.DateTime_GetDateTimePickerInfo
title: DateTime_GetDateTimePickerInfo macro (commctrl.h)
description: Gets information for a specified date and time picker (DTP) control.
helpviewer_keywords: ["DateTime_GetDateTimePickerInfo","DateTime_GetDateTimePickerInfo macro [Windows Controls]","_shell_DateTime_GetDateTimePickerInfo","_shell_DateTime_GetDateTimePickerInfo_cpp","commctrl/DateTime_GetDateTimePickerInfo","controls.DateTime_GetDateTimePickerInfo","controls._shell_DateTime_GetDateTimePickerInfo"]
old-location: controls\DateTime_GetDateTimePickerInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_getdatetimepickerinfo.htm
ms.date: 10/21/2024
ms.keywords: DateTime_GetDateTimePickerInfo, DateTime_GetDateTimePickerInfo macro [Windows Controls], _shell_DateTime_GetDateTimePickerInfo, _shell_DateTime_GetDateTimePickerInfo_cpp, commctrl/DateTime_GetDateTimePickerInfo, controls.DateTime_GetDateTimePickerInfo, controls._shell_DateTime_GetDateTimePickerInfo
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
 - DateTime_GetDateTimePickerInfo
 - commctrl/DateTime_GetDateTimePickerInfo
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
 - DateTime_GetDateTimePickerInfo
---

# DateTime_GetDateTimePickerInfo macro

## -syntax

```cpp
LRESULT DateTime_GetDateTimePickerInfo(
  [in]      HWND               hdp,
  [in, out] DATETIMEPICKERINFO *pdtpi
);
```

## -returns

Type: **[LRESULT](/windows/desktop/winprog/windows-data-types)**

Return value is ignored.


## -description

Gets information for a specified date and time picker (DTP) control.

## -parameters

### -param hdp [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the DTP control.

### -param pdtpi [in, out]

Type: <b><a href="/windows/desktop/api/commctrl/ns-commctrl-datetimepickerinfo">DATETIMEPICKERINFO</a>*</b>

<a href="/windows/desktop/api/commctrl/ns-commctrl-datetimepickerinfo">DATETIMEPICKERINFO</a>
<b>cbSize</b>
