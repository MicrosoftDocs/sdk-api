---
UID: NC:winnt.PFLS_CALLBACK_FUNCTION
title: PFLS_CALLBACK_FUNCTION
author: windows-sdk-content
description: An application-defined function. If the FLS slot is in use, FlsCallback is called on fiber deletion, thread exit, and when an FLS index is freed.
old-location: base\flscallback.htm
old-project: procthread
ms.assetid: d05a6550-7fec-44e6-9b38-dfafff7895c8
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: FlsCallback, FlsCallback callback function, PFLS_CALLBACK_FUNCTION, PFLS_CALLBACK_FUNCTION callback, _win32_flscallback, base.flscallback, winnt/FlsCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
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
req.typenames: NUMBERFMTW, *LPNUMBERFMTW
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PFLS_CALLBACK_FUNCTION callback function


## -description


An application-defined function. If the FLS slot is in use, <b>FlsCallback</b> is called on fiber deletion, thread exit, and when an FLS index is freed. Specify this function when calling the 
<a href="https://msdn.microsoft.com/dc348ef3-37e5-40f2-bd5c-5f8aebc7cc59">FlsAlloc</a> function. The <i>PFLS_CALLBACK_FUNCTION</i> type defines a pointer to this callback function. 
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




<a href="https://msdn.microsoft.com/6283f56b-23ae-4840-abd0-2478a50c670c">Fibers</a>



<a href="https://msdn.microsoft.com/dc348ef3-37e5-40f2-bd5c-5f8aebc7cc59">FlsAlloc</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

