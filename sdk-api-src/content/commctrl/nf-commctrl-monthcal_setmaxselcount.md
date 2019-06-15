---
UID: NF:commctrl.MonthCal_SetMaxSelCount
title: MonthCal_SetMaxSelCount macro (commctrl.h)
author: windows-sdk-content
description: Sets the maximum number of days that can be selected in a month calendar control. You can use this macro or send the MCM_SETMAXSELCOUNT message explicitly.
old-location: controls\MonthCal_SetMaxSelCount.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setmaxselcount.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MonthCal_SetMaxSelCount, MonthCal_SetMaxSelCount macro [Windows Controls], _win32_MonthCal_SetMaxSelCount, _win32_MonthCal_SetMaxSelCount_cpp, commctrl/MonthCal_SetMaxSelCount, controls.MonthCal_SetMaxSelCount, controls._win32_MonthCal_SetMaxSelCount
ms.topic: macro
f1_keywords: ["commctrl/MonthCal_SetMaxSelCount"]
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
 - MonthCal_SetMaxSelCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MonthCal_SetMaxSelCount macro


## -description


Sets the maximum number of days that can be selected in a month calendar control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/mcm-setmaxselcount">MCM_SETMAXSELCOUNT</a> message explicitly. 


## -parameters




### -param hmc

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle to a month calendar control. 


### -param n

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Value of type <b>int</b> that will be set to represent the maximum number of days that can be selected. 

