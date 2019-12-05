---
UID: NF:commctrl.DateTime_GetSystemtime
title: DateTime_GetSystemtime macro (commctrl.h)
description: Gets the currently selected time from a date and time picker (DTP) control and places it in a specified SYSTEMTIME structure. You can use this macro, or send the DTM_GETSYSTEMTIME message explicitly.
old-location: controls\DateTime_GetSystemtime.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_getsystemtime.htm
ms.date: 12/05/2018
ms.keywords: DateTime_GetSystemtime, DateTime_GetSystemtime macro [Windows Controls], _win32_DateTime_GetSystemtime, _win32_DateTime_GetSystemtime_cpp, commctrl/DateTime_GetSystemtime, controls.DateTime_GetSystemtime, controls._win32_DateTime_GetSystemtime
ms.topic: macro
f1_keywords:
- commctrl/DateTime_GetSystemtime
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
- DateTime_GetSystemtime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DateTime_GetSystemtime macro


## -description


Gets the currently selected time from a date and time picker (DTP) control and places it in a specified <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure. You can use this macro, or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/dtm-getsystemtime">DTM_GETSYSTEMTIME</a> message explicitly. 


## -parameters




### -param hdp

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a DTP control. 


### -param pst

Type: <b>LPSYSTEMTIME</b>

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure. If <a href="https://docs.microsoft.com/windows/desktop/Controls/dtm-getsystemtime">DTM_GETSYSTEMTIME</a> returns GDT_VALID, this structure will contain the currently selected time. Otherwise, it will not contain valid information. This parameter must be a valid pointer; it cannot be <b>NULL</b>. 

