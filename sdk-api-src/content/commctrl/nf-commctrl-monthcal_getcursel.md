---
UID: NF:commctrl.MonthCal_GetCurSel
title: MonthCal_GetCurSel macro
author: windows-sdk-content
description: Retrieves the currently selected date. You can use this macro or send the MCM_GETCURSEL message explicitly.
old-location: controls\MonthCal_GetCurSel.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_getcursel.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: MonthCal_GetCurSel, MonthCal_GetCurSel macro [Windows Controls], _win32_MonthCal_GetCurSel, _win32_MonthCal_GetCurSel_cpp, commctrl/MonthCal_GetCurSel, controls.MonthCal_GetCurSel, controls._win32_MonthCal_GetCurSel
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - MonthCal_GetCurSel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MonthCal_GetCurSel macro


## -description


Retrieves the currently selected date. You can use this macro or send the <a href="https://msdn.microsoft.com/d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f">MCM_GETCURSEL</a> message explicitly. 


## -parameters




### -param hmc

TBD


### -param pst

TBD






#### - hwndMC

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control. 


#### - lpSysTime

Type: <b>LPSYSTEMTIME</b>

Pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that will receive the currently selected date information. This parameter must be a valid address and cannot be <b>NULL</b>. 

