---
UID: NF:commctrl.MonthCal_SetCalendarBorder
title: MonthCal_SetCalendarBorder macro
author: windows-driver-content
description: Sets the border size, in pixels, of a month calendar control. You can use this macro or send the MCM_SETCALENDARBORDER message explicitly.
old-location: controls\MonthCal_SetCalendarBorder.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setcalendarborder.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: MonthCal_SetCalendarBorder, MonthCal_SetCalendarBorder macro [Windows Controls], _shell_MonthCal_SetCalendarBorder, _shell_MonthCal_SetCalendarBorder_cpp, commctrl/MonthCal_SetCalendarBorder, controls.MonthCal_SetCalendarBorder, controls._shell_MonthCal_SetCalendarBorder
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
-	MonthCal_SetCalendarBorder
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MonthCal_SetCalendarBorder macro


## -description


Sets the border size, in pixels, of a month calendar control. You can use this macro or send the <a href="https://msdn.microsoft.com/2a64a08f-a1fb-47a8-8f09-725807e87a03">MCM_SETCALENDARBORDER</a> message explicitly.


## -parameters




### -param hmc

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control.


### -param fset

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

If <b>TRUE</b>, then the border size is set to the number of pixels that <i>xyborder</i> specifies. If <b>FALSE</b>, then the border size is reset to the default value specified by the theme, or zero if themes are not being used.


### -param xyborder

Type: <b>int</b>

Number of pixels of the border size.

