---
UID: NF:commctrl.DateTime_CloseMonthCal
title: DateTime_CloseMonthCal macro
author: windows-sdk-content
description: Closes the date and time picker (DTP) control. Use this macro or send the DTM_CLOSEMONTHCAL message explicitly.
old-location: controls\DateTime_CloseMonthCal.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\datetime\macros\datetime_closemonthcal.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DateTime_CloseMonthCal, DateTime_CloseMonthCal macro [Windows Controls], _shell_DateTime_CloseMonthCal, _shell_DateTime_CloseMonthCal_cpp, commctrl/DateTime_CloseMonthCal, controls.DateTime_CloseMonthCal, controls._shell_DateTime_CloseMonthCal
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
 - DateTime_CloseMonthCal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- DateTime_CloseMonthCal
: 
---

# DateTime_CloseMonthCal macro


## -description


Closes the date and time picker (DTP) control. Use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761753(v=VS.85).aspx">DTM_CLOSEMONTHCAL</a> message explicitly.


## -parameters




### -param hdp

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the DTP control.


## -remarks



Destroys the control and sends a <a href="https://msdn.microsoft.com/en-us/library/Bb761735(v=VS.85).aspx">DTN_CLOSEUP</a> notification that the control is closing—as opposed to the control is opening (dropping-down as in the <a href="https://msdn.microsoft.com/en-us/library/Bb761739(v=VS.85).aspx">DTN_DROPDOWN</a> notification)—to the control's parent.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761735(v=VS.85).aspx">DTN_CLOSEUP</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb761739(v=VS.85).aspx">DTN_DROPDOWN</a>



<b>Reference</b>
 

 

