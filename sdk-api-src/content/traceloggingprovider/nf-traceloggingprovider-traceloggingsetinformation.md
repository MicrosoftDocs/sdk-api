---
UID: NF:traceloggingprovider.TraceLoggingSetInformation
title: TraceLoggingSetInformation function
author: windows-sdk-content
description: Provides special-purpose information to the Event Tracing for Windows (ETW) runtime.
old-location: tracelogging\traceloggingsetinformation.htm
old-project: tracelogging
ms.assetid: 7676DB80-6C4B-41EC-8FB5-8FD330D8ED49
ms.author: windowssdkdev
ms.date: 04/27/2018
ms.keywords: TraceLoggingSetInformation, TraceLoggingSetInformation function, tracelogging.traceloggingsetinformation, traceloggingprovider/TraceLoggingSetInformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: traceloggingprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2012 R2
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
req.typenames: TPMVSCMGR_ERROR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - N/A
api_name:
 - TraceLoggingSetInformation
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: N/A
req.irql: 
req.product: Windows XP with SP1 and later
---

# TraceLoggingSetInformation function


## -description


Provides special-purpose information to the Event Tracing for Windows (ETW) runtime.


## -parameters




### -param hProvider [in, out]

Handle to the provider.


### -param informationClass [in]

The type of information for the provider.


### -param pvInformation [in]

The input buffer.


### -param cbInformation [in]

The size of the input buffer.


## -returns



If you call this function from user mode code, the function returns a HRESULT. Use the SUCCEEDED() macro to determine if the function succeeds.

 If you call this function from kernel mode code, the function returns a NTSTATUS. Use the NT_SUCCESS() macro to determine if the function succeeds.




## -remarks



This function serves as a wrapper around the <a href="https://msdn.microsoft.com/e8b408ba-4bb5-4166-bf43-d18e4fe8de32">EventSetInformation</a> function.

To control the behavior of this function, use macros TLG_EVENT_SET_INFORMATION and TLG_HAVE_EVENT_SET_INFORMATION.



