---
UID: NF:commctrl.MonthCal_GetMaxSelCount
title: MonthCal_GetMaxSelCount macro (commctrl.h)
description: Retrieves the maximum date range that can be selected in a month calendar control. You can use this macro or send the MCM_GETMAXSELCOUNT message explicitly.helpviewer_keywords: ["MonthCal_GetMaxSelCount","MonthCal_GetMaxSelCount macro [Windows Controls]","_win32_MonthCal_GetMaxSelCount","_win32_MonthCal_GetMaxSelCount_cpp","commctrl/MonthCal_GetMaxSelCount","controls.MonthCal_GetMaxSelCount","controls._win32_MonthCal_GetMaxSelCount"]
old-location: controls\MonthCal_GetMaxSelCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getmaxselcount.htm
ms.date: 12/05/2018
ms.keywords: MonthCal_GetMaxSelCount, MonthCal_GetMaxSelCount macro [Windows Controls], _win32_MonthCal_GetMaxSelCount, _win32_MonthCal_GetMaxSelCount_cpp, commctrl/MonthCal_GetMaxSelCount, controls.MonthCal_GetMaxSelCount, controls._win32_MonthCal_GetMaxSelCount
f1_keywords:
- commctrl/MonthCal_GetMaxSelCount
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
- MonthCal_GetMaxSelCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MonthCal_GetMaxSelCount macro


## -description


Retrieves the maximum date range that can be selected in a month calendar control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/mcm-getmaxselcount">MCM_GETMAXSELCOUNT</a> message explicitly. 


## -parameters




### -param hmc

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control. 


## -remarks



You can change the maximum date range that can be selected by using the <a href="https://docs.microsoft.com/windows/desktop/Controls/mcm-setmaxselcount">MCM_SETMAXSELCOUNT</a> message. 



