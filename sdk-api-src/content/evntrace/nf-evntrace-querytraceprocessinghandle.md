---
UID: NF:evntrace.QueryTraceProcessingHandle
title: QueryTraceProcessingHandle function
author: windows-sdk-content
description: Queries the system for the trace processing handle.
old-location: etw\querytraceprocessinghandle.htm
tech.root: ETW
ms.assetid: 87666275-8752-4EC8-9C01-16D36AE4C5E8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: QueryTraceProcessingHandle, QueryTraceProcessingHandle function [ETW], etw.querytraceprocessinghandle, evntrace/QueryTraceProcessingHandle
ms.topic: function
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: AdvAPI32.lib
req.dll: AdvAPI32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - AdvAPI32.dll
 - Sechost.dll
api_name:
 - QueryTraceProcessingHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# QueryTraceProcessingHandle function


## -description


Queries the system for the trace processing handle.


## -parameters




### -param ProcessingHandle [in]

A valid handle created with <a href="https://msdn.microsoft.com/505e643b-6b4f-4f93-96c8-7fe8abdd6234">OpenTrace</a> that the data should be queried from.


### -param InformationClass [in]

An <a href="https://msdn.microsoft.com/92932E4C-0A06-4CDE-B14B-BF53226E133B">ETW_PROCESS_HANDLE_INFO_TYPE</a> value that specifies what kind of operation will be done on the handle.


### -param InBuffer [in, optional]

Reserved for future use. May be null.


### -param InBufferSize [in]

Size in bytes of the <i>InBuffer</i>.


### -param OutBuffer [out, optional]

Buffer provided by the caller to contain output data.


### -param OutBufferSize [in]

Size in bytes of <i>OutBuffer.</i>


### -param ReturnLength [out]

The size in bytes of the data that the API wrote into <i>OutBuffer</i>.  Important for variable length returns.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>. 



