---
UID: NF:commctrl.DateTime_CloseMonthCal
title: DateTime_CloseMonthCal macro (commctrl.h)
description: Closes the date and time picker (DTP) control. Use this macro or send the DTM_CLOSEMONTHCAL message explicitly.
helpviewer_keywords: ["DateTime_CloseMonthCal","DateTime_CloseMonthCal macro [Windows Controls]","_shell_DateTime_CloseMonthCal","_shell_DateTime_CloseMonthCal_cpp","commctrl/DateTime_CloseMonthCal","controls.DateTime_CloseMonthCal","controls._shell_DateTime_CloseMonthCal"]
old-location: controls\DateTime_CloseMonthCal.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_closemonthcal.htm
ms.date: 10/21/2024
ms.keywords: DateTime_CloseMonthCal, DateTime_CloseMonthCal macro [Windows Controls], _shell_DateTime_CloseMonthCal, _shell_DateTime_CloseMonthCal_cpp, commctrl/DateTime_CloseMonthCal, controls.DateTime_CloseMonthCal, controls._shell_DateTime_CloseMonthCal
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
 - DateTime_CloseMonthCal
 - commctrl/DateTime_CloseMonthCal
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
 - DateTime_CloseMonthCal
---

# DateTime_CloseMonthCal macro

## -syntax

```cpp
LRESULT DateTime_CloseMonthCal(
   HWND hdp
);
```

## -returns

Type: **[LRESULT](/windows/desktop/winprog/windows-data-types)**

Returns zero.


## -description

Closes the date and time picker (DTP) control. Use this macro or send the <a href="/windows/desktop/Controls/dtm-closemonthcal">DTM_CLOSEMONTHCAL</a> message explicitly.

## -parameters

### -param hdp

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the DTP control.

## -remarks

Destroys the control and sends a <a href="/windows/desktop/Controls/dtn-closeup">DTN_CLOSEUP</a> notification that the control is closing—as opposed to the control is opening (dropping-down as in the <a href="/windows/desktop/Controls/dtn-dropdown">DTN_DROPDOWN</a> notification)—to the control's parent.

## -see-also

<a href="/windows/desktop/Controls/dtn-closeup">DTN_CLOSEUP</a>



<a href="/windows/desktop/Controls/dtn-dropdown">DTN_DROPDOWN</a>



<b>Reference</b>
