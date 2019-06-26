---
UID: NF:winbase.IsSystemResumeAutomatic
title: IsSystemResumeAutomatic function (winbase.h)
author: windows-sdk-content
description: Determines the current state of the computer.
old-location: base\issystemresumeautomatic.htm
tech.root: power
ms.assetid: fc9d69cf-26cf-4973-a154-1acb26773738
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IsSystemResumeAutomatic, IsSystemResumeAutomatic function, _win32_issystemresumeautomatic, base.issystemresumeautomatic, winbase/IsSystemResumeAutomatic
ms.topic: function
f1_keywords: 
 - "winbase/IsSystemResumeAutomatic"
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - IsSystemResumeAutomatic
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IsSystemResumeAutomatic function


## -description


Determines the current state of the computer.


## -parameters






## -returns



If the system was restored to the working state automatically and the user is not active, the function returns <b>TRUE</b>. Otherwise, the function returns <b>FALSE</b>.




## -remarks



The 
<a href="https://docs.microsoft.com/windows/desktop/Power/pbt-apmresumeautomatic">PBT_APMRESUMEAUTOMATIC</a> event is broadcast when the system wakes automatically to handle an event. The user is generally not present. If the system detects any user activity after broadcasting the 
PBT_APMRESUMEAUTOMATIC event, it will broadcast the 
<a href="https://docs.microsoft.com/windows/desktop/Power/pbt-apmresumesuspend">PBT_APMRESUMESUSPEND</a> event to let applications know they can resume full interaction with the user.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Power/pbt-apmresumeautomatic">PBT_APMRESUMEAUTOMATIC</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/pbt-apmresumesuspend">PBT_APMRESUMESUSPEND</a>



<a href="https://docs.microsoft.com/windows/desktop/Power/power-management-functions">Power Management Functions</a>
 

 

