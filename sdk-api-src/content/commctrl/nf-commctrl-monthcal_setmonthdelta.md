---
UID: NF:commctrl.MonthCal_SetMonthDelta
title: MonthCal_SetMonthDelta macro
author: windows-sdk-content
description: Sets the scroll rate for a month calendar control. The scroll rate is the number of months that the control moves its display when the user clicks a scroll button. You can use this macro or send the MCM_SETMONTHDELTA message explicitly.
old-location: controls\MonthCal_SetMonthDelta.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setmonthdelta.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MonthCal_SetMonthDelta, MonthCal_SetMonthDelta macro [Windows Controls], _win32_MonthCal_SetMonthDelta, _win32_MonthCal_SetMonthDelta_cpp, commctrl/MonthCal_SetMonthDelta, controls.MonthCal_SetMonthDelta, controls._win32_MonthCal_SetMonthDelta
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
 - MonthCal_SetMonthDelta
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MonthCal_SetMonthDelta macro


## -description


Sets the scroll rate for a month calendar control. The scroll rate is the number of months that the control moves its display when the user clicks a scroll button. You can use this macro or send the <a href="https://msdn.microsoft.com/2d01b95f-3be8-4548-80b5-ac01d3e49e9f">MCM_SETMONTHDELTA</a> message explicitly. 


## -parameters




### -param hmc

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control. 


### -param n

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

Value representing the number of months to be set as the control's scroll rate. If this value is zero, the month delta is reset to the default, which is the number of months displayed in the control. 


## -remarks



The PAGE UP and PAGE DOWN keys, VK_PRIOR and VK_NEXT, change the selected month by one, regardless of the number of months displayed or the value set by <a href="https://msdn.microsoft.com/2d01b95f-3be8-4548-80b5-ac01d3e49e9f">MCM_SETMONTHDELTA</a>.



