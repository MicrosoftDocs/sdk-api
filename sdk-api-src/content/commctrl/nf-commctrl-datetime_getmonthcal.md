---
UID: NF:commctrl.DateTime_GetMonthCal
title: DateTime_GetMonthCal macro (commctrl.h)
description: Gets the handle to a date and time picker's (DTP) child month calendar control. You can use this macro or send the DTM_GETMONTHCAL message explicitly.helpviewer_keywords: ["DateTime_GetMonthCal","DateTime_GetMonthCal macro [Windows Controls]","_win32_DateTime_GetMonthCal","_win32_DateTime_GetMonthCal_cpp","commctrl/DateTime_GetMonthCal","controls.DateTime_GetMonthCal","controls._win32_DateTime_GetMonthCal"]
old-location: controls\DateTime_GetMonthCal.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_getmonthcal.htm
ms.date: 12/05/2018
ms.keywords: DateTime_GetMonthCal, DateTime_GetMonthCal macro [Windows Controls], _win32_DateTime_GetMonthCal, _win32_DateTime_GetMonthCal_cpp, commctrl/DateTime_GetMonthCal, controls.DateTime_GetMonthCal, controls._win32_DateTime_GetMonthCal
f1_keywords:
- commctrl/DateTime_GetMonthCal
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Commctrl.h
api_name:
- DateTime_GetMonthCal
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DateTime_GetMonthCal macro


## -description


Gets the handle to a date and time picker's (DTP) child month calendar control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/dtm-getmonthcal">DTM_GETMONTHCAL</a> message explicitly. 


## -parameters




### -param hdp

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a DTP control. 


## -remarks



DTP controls create a child month calendar control when the user clicks the drop-down arrow (<a href="https://docs.microsoft.com/windows/desktop/Controls/dtn-dropdown">DTN_DROPDOWN</a> notification). When the month calendar is no longer needed, it is destroyed (a <a href="https://docs.microsoft.com/windows/desktop/Controls/dtn-closeup">DTN_CLOSEUP</a> notification is sent on destruction). So your application must not rely on a static handle to the DTP's child month calendar. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/dtn-closeup">DTN_CLOSEUP</a>



<a href="https://docs.microsoft.com/windows/desktop/Controls/dtn-dropdown">DTN_DROPDOWN</a>



<b>Reference</b>
 

 

