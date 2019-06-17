---
UID: NC:winnt.PFLS_CALLBACK_FUNCTION
title: PFLS_CALLBACK_FUNCTION (winnt.h)
author: windows-sdk-content
description: An application-defined function. If the FLS slot is in use, FlsCallback is called on fiber deletion, thread exit, and when an FLS index is freed.
old-location: base\flscallback.htm
tech.root: ProcThread
ms.assetid: d05a6550-7fec-44e6-9b38-dfafff7895c8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FlsCallback, FlsCallback callback function, PFLS_CALLBACK_FUNCTION, PFLS_CALLBACK_FUNCTION callback, _win32_flscallback, base.flscallback, winnt/FlsCallback
ms.topic: callback
f1_keywords: ["winnt/FlsCallback"]
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - Winnt.h
api_name:
 - FlsCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PFLS_CALLBACK_FUNCTION callback function


## -description


An application-defined function. If the FLS slot is in use, <b>FlsCallback</b> is called on fiber deletion, thread exit, and when an FLS index is freed. Specify this function when calling the 
<a href="https://docs.microsoft.com/windows/desktop/api/fibersapi/nf-fibersapi-flsalloc">FlsAlloc</a> function. The <i>PFLS_CALLBACK_FUNCTION</i> type defines a pointer to this callback function. 
<b>FlsCallback</b> is a placeholder for the application-defined function name.


## -parameters




### -param lpFlsData [in]

The value stored in the FLS slot for the calling fiber.


## -returns



This function does not return a value.




## -remarks



Each FLS index has an associated 
<b>FlsCallback</b> function. The callback function can be used for any purpose, but it is intended to be used primarily to free memory.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ProcThread/fibers">Fibers</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fibersapi/nf-fibersapi-flsalloc">FlsAlloc</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>
 

 

