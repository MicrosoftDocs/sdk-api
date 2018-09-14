---
UID: NF:commctrl.MonthCal_SetCALID
title: MonthCal_SetCALID macro
author: windows-sdk-content
description: Sets the calendar ID for the given calendar control. You can use this macro or send the MCM_SETCALID message explicitly.
old-location: controls\MonthCal_SetCALID.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setcalid.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: MonthCal_SetCALID, MonthCal_SetCALID macro [Windows Controls], _shell_MonthCal_SetCALID, _shell_MonthCal_SetCALID_cpp, commctrl/MonthCal_SetCALID, controls.MonthCal_SetCALID, controls._shell_MonthCal_SetCALID
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
 - MonthCal_SetCALID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MonthCal_SetCALID macro


## -description


Sets the calendar ID for the given calendar control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb760995(v=VS.85).aspx">MCM_SETCALID</a> message explicitly.


## -parameters




### -param hmc

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

Handle to a month calendar control.


### -param calid

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT</a></b>

Calendar ID. One of the <a href="https://msdn.microsoft.com/en-us/library/Dd317732(v=VS.85).aspx">Calendar Identifiers</a> constants.

