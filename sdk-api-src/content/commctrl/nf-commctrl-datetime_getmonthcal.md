---
UID: NF:commctrl.DateTime_GetMonthCal
title: DateTime_GetMonthCal macro
author: windows-sdk-content
description: Gets the handle to a date and time picker's (DTP) child month calendar control. You can use this macro or send the DTM_GETMONTHCAL message explicitly.
old-location: controls\DateTime_GetMonthCal.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_getmonthcal.htm
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: DateTime_GetMonthCal, DateTime_GetMonthCal macro [Windows Controls], _win32_DateTime_GetMonthCal, _win32_DateTime_GetMonthCal_cpp, commctrl/DateTime_GetMonthCal, controls.DateTime_GetMonthCal, controls._win32_DateTime_GetMonthCal
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
 - DateTime_GetMonthCal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# DateTime_GetMonthCal macro


## -description


Gets the handle to a date and time picker's (DTP) child month calendar control. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb761765(v=VS.85).aspx">DTM_GETMONTHCAL</a> message explicitly. 


## -parameters




### -param hdp

TBD






#### - hwndDP

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a DTP control. 


## -remarks



DTP controls create a child month calendar control when the user clicks the drop-down arrow (<a href="https://msdn.microsoft.com/library/Bb761739(v=VS.85).aspx">DTN_DROPDOWN</a> notification). When the month calendar is no longer needed, it is destroyed (a <a href="https://msdn.microsoft.com/library/Bb761735(v=VS.85).aspx">DTN_CLOSEUP</a> notification is sent on destruction). So your application must not rely on a static handle to the DTP's child month calendar. 




## -see-also




<a href="https://msdn.microsoft.com/library/Bb761735(v=VS.85).aspx">DTN_CLOSEUP</a>



<a href="https://msdn.microsoft.com/library/Bb761739(v=VS.85).aspx">DTN_DROPDOWN</a>



<b>Reference</b>
 

 

