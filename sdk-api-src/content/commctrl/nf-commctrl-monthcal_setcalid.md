---
UID: NF:commctrl.MonthCal_SetCALID
title: MonthCal_SetCALID macro
author: windows-sdk-content
description: Sets the calendar ID for the given calendar control. You can use this macro or send the MCM_SETCALID message explicitly.
old-location: controls\MonthCal_SetCALID.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\monthcal\macros\monthcal_setcalid.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MonthCal_SetCALID, MonthCal_SetCALID macro [Windows Controls], _shell_MonthCal_SetCALID, _shell_MonthCal_SetCALID_cpp, commctrl/MonthCal_SetCALID, controls.MonthCal_SetCALID, controls._shell_MonthCal_SetCALID
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
 - MonthCal_SetCALID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# MonthCal_SetCALID macro


## -description


Sets the calendar ID for the given calendar control. You can use this macro or send the <a href="https://msdn.microsoft.com/4b9d06f5-0784-4a17-b401-982206d4be67">MCM_SETCALID</a> message explicitly.


## -parameters




### -param hmc

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control.


### -param calid

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Calendar ID. One of the <a href="https://msdn.microsoft.com/ba2e841e-e24e-476a-851e-a29b3af4f04d">Calendar Identifiers</a> constants.

