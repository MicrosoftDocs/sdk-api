---
UID: NF:commctrl.DateTime_GetMonthCalStyle
title: DateTime_GetMonthCalStyle macro (commctrl.h)
description: Gets the style of a specified date and time picker (DTP) control. Use this macro or send the DTM_GETMCSTYLE message explicitly.
helpviewer_keywords: ["DateTime_GetMonthCalStyle","DateTime_GetMonthCalStyle macro [Windows Controls]","_shell_DateTime_GetMonthCalStyle","_shell_DateTime_GetMonthCalStyle_cpp","commctrl/DateTime_GetMonthCalStyle","controls.DateTime_GetMonthCalStyle","controls._shell_DateTime_GetMonthCalStyle"]
old-location: controls\DateTime_GetMonthCalStyle.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_getmonthcalstyle.htm
ms.date: 10/21/2024
ms.keywords: DateTime_GetMonthCalStyle, DateTime_GetMonthCalStyle macro [Windows Controls], _shell_DateTime_GetMonthCalStyle, _shell_DateTime_GetMonthCalStyle_cpp, commctrl/DateTime_GetMonthCalStyle, controls.DateTime_GetMonthCalStyle, controls._shell_DateTime_GetMonthCalStyle
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
 - DateTime_GetMonthCalStyle
 - commctrl/DateTime_GetMonthCalStyle
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
 - DateTime_GetMonthCalStyle
---

# DateTime_GetMonthCalStyle macro

## -syntax

```cpp
LRESULT DateTime_GetMonthCalStyle(
  [in] HWND hdp
);
```

## -returns

Type: **[LRESULT](/windows/desktop/winprog/windows-data-types)**

Returns the style value of the control. For more information see Month Calendar Control Styles.


## -description

Gets the style of a specified date and time picker (DTP) control. Use this macro or send the <a href="/windows/desktop/Controls/dtm-getmcstyle">DTM_GETMCSTYLE</a> message explicitly.

## -parameters

### -param hdp [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the DTP control.
