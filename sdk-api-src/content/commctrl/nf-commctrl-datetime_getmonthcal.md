---
UID: NF:commctrl.DateTime_GetMonthCal
title: DateTime_GetMonthCal macro
author: windows-sdk-content
description: Gets the handle to a date and time picker's (DTP) child month calendar control. You can use this macro or send the DTM_GETMONTHCAL message explicitly.
old-location: controls\DateTime_GetMonthCal.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_getmonthcal.htm
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: DateTime_GetMonthCal, DateTime_GetMonthCal macro [Windows Controls], _win32_DateTime_GetMonthCal, _win32_DateTime_GetMonthCal_cpp, commctrl/DateTime_GetMonthCal, controls.DateTime_GetMonthCal, controls._win32_DateTime_GetMonthCal
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
 - DateTime_GetMonthCal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DateTime_GetMonthCal macro


## -description


Gets the handle to a date and time picker's (DTP) child month calendar control. You can use this macro or send the <a href="https://msdn.microsoft.com/78bbdcc9-2b2b-420b-be9b-6f2f573d60b6">DTM_GETMONTHCAL</a> message explicitly. 


## -parameters




### -param hdp

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a DTP control. 


## -remarks



DTP controls create a child month calendar control when the user clicks the drop-down arrow (<a href="https://msdn.microsoft.com/6f20fa87-2223-4876-b77d-2c684685bf10">DTN_DROPDOWN</a> notification). When the month calendar is no longer needed, it is destroyed (a <a href="https://msdn.microsoft.com/94ace714-55cc-4c59-8b87-8d0348b15f34">DTN_CLOSEUP</a> notification is sent on destruction). So your application must not rely on a static handle to the DTP's child month calendar. 




## -see-also




<a href="https://msdn.microsoft.com/94ace714-55cc-4c59-8b87-8d0348b15f34">DTN_CLOSEUP</a>



<a href="https://msdn.microsoft.com/6f20fa87-2223-4876-b77d-2c684685bf10">DTN_DROPDOWN</a>



<b>Reference</b>
 

 

