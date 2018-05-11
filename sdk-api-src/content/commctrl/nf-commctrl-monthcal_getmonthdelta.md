---
UID: NF:commctrl.MonthCal_GetMonthDelta
title: MonthCal_GetMonthDelta macro
author: windows-driver-content
description: Retrieves the scroll rate for a month calendar control. The scroll rate is the number of months that the control moves its display when the user clicks a scroll button. You can use this macro or send the MCM_GETMONTHDELTA message explicitly.
old-location: controls\MonthCal_GetMonthDelta.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getmonthdelta.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MonthCal_GetMonthDelta, MonthCal_GetMonthDelta macro [Windows Controls], _win32_MonthCal_GetMonthDelta, _win32_MonthCal_GetMonthDelta_cpp, commctrl/MonthCal_GetMonthDelta, controls.MonthCal_GetMonthDelta, controls._win32_MonthCal_GetMonthDelta
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	MonthCal_GetMonthDelta
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MonthCal_GetMonthDelta macro


## -description


Retrieves the scroll rate for a month calendar control. The scroll rate is the number of months that the control moves its display when the user clicks a scroll button. You can use this macro or send the <a href="https://msdn.microsoft.com/6db02993-b22c-430f-8928-8bd5768b2151">MCM_GETMONTHDELTA</a> message explicitly. 


## -parameters




### -param hmc

TBD






#### - hwndMC

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control. 

