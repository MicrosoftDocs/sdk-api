---
UID: NF:objbase.CoFileTimeToDosDateTime
title: CoFileTimeToDosDateTime function
author: windows-sdk-content
description: Converts a FILETIME into MS-DOS date and time values.
old-location: com\cofiletimetodosdatetime.htm
tech.root: com
ms.assetid: 38670fe7-10cf-44e2-a5f1-60ec43fd83b5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CoFileTimeToDosDateTime, CoFileTimeToDosDateTime function [COM], _com_CoFileTimeToDosDateTime, com.cofiletimetodosdatetime, objbase/CoFileTimeToDosDateTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: objbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
api_name:
 - CoFileTimeToDosDateTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CoFileTimeToDosDateTime function


## -description


Converts a <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> into MS-DOS date and time values.
<div class="alert"><b>Note</b>  This function is provided for compatibility with 16-bit Windows.</div><div> </div>

## -parameters




### -param lpFileTime [in]

A pointer to the <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.


### -param lpDosDate [out]

Receives the MS-DOS date.


### -param lpDosTime [out]

Receives the MS-DOS time.


## -returns



If the function succeeds, the return value is <b>TRUE</b>; otherwise, it is <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/eb7af6a3-7547-405e-b96e-3e68a1ac273b">CoDosDateTimeToFileTime</a>



<a href="https://msdn.microsoft.com/00083429-1d61-4a0b-bb73-82158869466d">CoFileTimeNow</a>
 

 

