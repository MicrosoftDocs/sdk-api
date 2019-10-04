---
UID: NF:commctrl.MonthCal_GetCurSel
title: MonthCal_GetCurSel macro (commctrl.h)
author: windows-sdk-content
description: Retrieves the currently selected date. You can use this macro or send the MCM_GETCURSEL message explicitly.
old-location: controls\MonthCal_GetCurSel.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getcursel.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MonthCal_GetCurSel, MonthCal_GetCurSel macro [Windows Controls], _win32_MonthCal_GetCurSel, _win32_MonthCal_GetCurSel_cpp, commctrl/MonthCal_GetCurSel, controls.MonthCal_GetCurSel, controls._win32_MonthCal_GetCurSel
ms.topic: macro
f1_keywords: 
 - "commctrl/MonthCal_GetCurSel"
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
 - MonthCal_GetCurSel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MonthCal_GetCurSel macro


## -description


Retrieves the currently selected date. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/mcm-getcursel">MCM_GETCURSEL</a> message explicitly. 


## -parameters




### -param hmc

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control. 


### -param pst

Type: <b>LPSYSTEMTIME</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that will receive the currently selected date information. This parameter must be a valid address and cannot be <b>NULL</b>. 

