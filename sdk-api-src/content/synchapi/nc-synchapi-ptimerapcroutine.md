---
UID: NC:synchapi.PTIMERAPCROUTINE
title: PTIMERAPCROUTINE
author: windows-sdk-content
description: An application-defined timer completion routine. Specify this address when calling the SetWaitableTimer function.
old-location: base\timerapcproc.htm
tech.root: sync
ms.assetid: 4e9f7bee-9c39-40d2-8588-0b3a1d7f9ede
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PTIMERAPCROUTINE, PTIMERAPCROUTINE callback, PTIMERAPCROUTINE callback function, _win32_timerapcproc, base.timerapcproc, synchapi/PTIMERAPCROUTINE
ms.topic: callback
req.header: synchapi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - synchapi.h
api_name:
 - PTIMERAPCROUTINE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PTIMERAPCROUTINE callback function


## -description


An application-defined timer completion routine. Specify this address when calling the 
<a href="https://msdn.microsoft.com/237e22dc-696d-473f-8bb5-c28f7c7c75b2">SetWaitableTimer</a> function. The <b>PTIMERAPCROUTINE</b> type defines a pointer to this callback function. 
<b>TimerAPCProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param lpArgToCompletionRoutine [in, optional]

The value passed to the function using the <i>lpArgToCompletionRoutine</i> parameter of the 
<a href="https://msdn.microsoft.com/237e22dc-696d-473f-8bb5-c28f7c7c75b2">SetWaitableTimer</a> function.


### -param dwTimerLowValue [in]

The low-order portion of the UTC-based time at which the timer was signaled. This value corresponds to the <b>dwLowDateTime</b> member of the 
<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure. For more information about UTC-based time, see 
<a href="https://msdn.microsoft.com/1a1e251e-2375-4134-bbd8-1e4670b9f9d2">System Time</a>.


### -param dwTimerHighValue [in]

The high-order portion of the UTC-based time at which the timer was signaled. This value corresponds to the <b>dwHighDateTime</b> member of the <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> structure.


## -returns



This function does not return a value.




## -remarks



The completion routine is executed by the thread that activates the timer using 
<a href="https://msdn.microsoft.com/237e22dc-696d-473f-8bb5-c28f7c7c75b2">SetWaitableTimer</a>. However, the thread must be in an alertable state. For more information, see 
<a href="https://msdn.microsoft.com/0197d78e-a4dc-414b-88ba-c5ec5f2ed614">Asynchronous Procedure Calls</a>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/aea3c080-caf2-4c16-adc5-51357a0340b8">Using a Waitable Timer with an Asynchronous Procedure Call</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/237e22dc-696d-473f-8bb5-c28f7c7c75b2">SetWaitableTimer</a>
 

 

