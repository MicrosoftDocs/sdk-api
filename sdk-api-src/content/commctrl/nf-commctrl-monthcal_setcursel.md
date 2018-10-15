---
UID: NF:commctrl.MonthCal_SetCurSel
title: MonthCal_SetCurSel macro
author: windows-sdk-content
description: Sets the currently selected date for a month calendar control. If the specified date is not in view, the control updates the display to bring it into view. You can use this macro or send the MCM_SETCURSEL message explicitly.
old-location: controls\MonthCal_SetCurSel.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setcursel.htm
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: MonthCal_SetCurSel, MonthCal_SetCurSel macro [Windows Controls], _win32_MonthCal_SetCurSel, _win32_MonthCal_SetCurSel_cpp, commctrl/MonthCal_SetCurSel, controls.MonthCal_SetCurSel, controls._win32_MonthCal_SetCurSel
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
 - MonthCal_SetCurSel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MonthCal_SetCurSel macro


## -description


Sets the currently selected date for a month calendar control. If the specified date is not in view, the control updates the display to bring it into view. You can use this macro or send the <a href="https://msdn.microsoft.com/2a9f82a1-66d9-44dd-b60f-b588b4688316">MCM_SETCURSEL</a> message explicitly. 


## -parameters




### -param hmc

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control. 


### -param pst

Type: <b>LPSYSTEMTIME</b>

Pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure that contains the date to be set as the current selection. The time members of this structure are ignored. 

