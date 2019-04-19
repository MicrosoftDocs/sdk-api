---
UID: NF:winbase.DeregisterEventSource
title: DeregisterEventSource function (winbase.h)
author: windows-sdk-content
description: Closes the specified event log.
old-location: base\deregistereventsource.htm
tech.root: EventLog
ms.assetid: f5d1f4b0-5320-4aec-a129-cafff6f1fed1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeregisterEventSource, DeregisterEventSource function, _win32_deregistereventsource, base.deregistereventsource, winbase/DeregisterEventSource
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-EventLog-Legacy-l1-1-0.dll
 - advapi32legacy.dll
 - Ext-MS-Win-AdvAPI32-EventLog-l1-1-0.dll
 - Ext-Ms-Win-AdvAPI32-EventLog-L1-1-1.dll
api_name:
 - DeregisterEventSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DeregisterEventSource function


## -description


Closes the specified event log.


## -parameters




### -param hEventLog [in, out]

A handle to the event log. The 
<a href="https://msdn.microsoft.com/53706f83-6bc9-45d6-981c-bd0680d7bc08">RegisterEventSource</a> function returns this handle.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/fd5c12ec-3a3d-4b75-a573-0b27ae7a890b">Event Logging Functions</a>



<a href="https://msdn.microsoft.com/bc7fdc74-be41-4d17-997c-27171ef73f0f">Event Sources</a>



<a href="https://msdn.microsoft.com/53706f83-6bc9-45d6-981c-bd0680d7bc08">RegisterEventSource</a>
 

 

