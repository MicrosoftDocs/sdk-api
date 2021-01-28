---
UID: NC:synchapi.PTIMERAPCROUTINE
title: PTIMERAPCROUTINE (synchapi.h)
description: An application-defined timer completion routine. Specify this address when calling the SetWaitableTimer function.
helpviewer_keywords: ["PTIMERAPCROUTINE","PTIMERAPCROUTINE callback","PTIMERAPCROUTINE callback function","_win32_timerapcproc","base.timerapcproc","synchapi/PTIMERAPCROUTINE"]
old-location: base\timerapcproc.htm
tech.root: base
ms.assetid: 4e9f7bee-9c39-40d2-8588-0b3a1d7f9ede
ms.date: 12/05/2018
ms.keywords: PTIMERAPCROUTINE, PTIMERAPCROUTINE callback, PTIMERAPCROUTINE callback function, _win32_timerapcproc, base.timerapcproc, synchapi/PTIMERAPCROUTINE
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PTIMERAPCROUTINE
 - synchapi/PTIMERAPCROUTINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - synchapi.h
api_name:
 - PTIMERAPCROUTINE
---

# PTIMERAPCROUTINE callback function


## -description

An application-defined timer completion routine. Specify this address when calling the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer">SetWaitableTimer</a> function. The <b>PTIMERAPCROUTINE</b> type defines a pointer to this callback function. 
<b>TimerAPCProc</b> is a placeholder for the application-defined function name.

## -parameters

### -param lpArgToCompletionRoutine [in, optional]

The value passed to the function using the <i>lpArgToCompletionRoutine</i> parameter of the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer">SetWaitableTimer</a> function.

### -param dwTimerLowValue [in]

The low-order portion of the UTC-based time at which the timer was signaled. This value corresponds to the <b>dwLowDateTime</b> member of the 
<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure. For more information about UTC-based time, see 
<a href="/windows/desktop/SysInfo/system-time">System Time</a>.

### -param dwTimerHighValue [in]

The high-order portion of the UTC-based time at which the timer was signaled. This value corresponds to the <b>dwHighDateTime</b> member of the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.

## -remarks

The completion routine is executed by the thread that activates the timer using 
<a href="/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer">SetWaitableTimer</a>. However, the thread must be in an alertable state. For more information, see 
<a href="/windows/desktop/Sync/asynchronous-procedure-calls">Asynchronous Procedure Calls</a>.


#### Examples

For an example, see 
<a href="/windows/desktop/Sync/using-a-waitable-timer-with-an-asynchronous-procedure-call">Using a Waitable Timer with an Asynchronous Procedure Call</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer">SetWaitableTimer</a>