---
UID: NF:commctrl.MonthCal_SetCalendarBorder
title: MonthCal_SetCalendarBorder macro
author: windows-sdk-content
description: Sets the border size, in pixels, of a month calendar control. You can use this macro or send the MCM_SETCALENDARBORDER message explicitly.
old-location: controls\MonthCal_SetCalendarBorder.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setcalendarborder.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: MonthCal_SetCalendarBorder, MonthCal_SetCalendarBorder macro [Windows Controls], _shell_MonthCal_SetCalendarBorder, _shell_MonthCal_SetCalendarBorder_cpp, commctrl/MonthCal_SetCalendarBorder, controls.MonthCal_SetCalendarBorder, controls._shell_MonthCal_SetCalendarBorder
ms.prod: windows
ms.technology: windows-sdk
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
 - MonthCal_SetCalendarBorder
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MonthCal_SetCalendarBorder macro


## -description


Sets the border size, in pixels, of a month calendar control. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb760993(v=VS.85).aspx">MCM_SETCALENDARBORDER</a> message explicitly.


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

