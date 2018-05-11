---
UID: NF:commctrl.MonthCal_SetSelRange
title: MonthCal_SetSelRange macro
author: windows-driver-content
description: Sets the selection for a month calendar control to a given date range. You can use this macro or send the MCM_SETSELRANGE message explicitly.
old-location: controls\MonthCal_SetSelRange.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setselrange.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MonthCal_SetSelRange, MonthCal_SetSelRange macro [Windows Controls], _win32_MonthCal_SetSelRange, _win32_MonthCal_SetSelRange_cpp, commctrl/MonthCal_SetSelRange, controls.MonthCal_SetSelRange, controls._win32_MonthCal_SetSelRange
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
-	MonthCal_SetSelRange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MonthCal_SetSelRange macro


## -description


Sets the selection for a month calendar control to a given date range. You can use this macro or send the <a href="https://msdn.microsoft.com/750b0c83-6baa-4caa-a738-feae8751a70e">MCM_SETSELRANGE</a> message explicitly. 


## -parameters




### -param hmc

TBD


### -param rgst

TBD






#### - hwndMC

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control. 


#### - lprgSysTimeArray

Type: <b>LPSYSTEMTIME</b>

Pointer to a two-element array of <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structures that contain date information representing the selection limits. The first selected date must be specified in <i>lprgSysTimeArray</i>[0], and the last selected date must be specified in <i>lprgSysTimeArray</i>[1]. The time members of these structures are ignored. 

