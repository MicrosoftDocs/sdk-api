---
UID: NF:evntrace.QueryTraceProcessingHandle
title: QueryTraceProcessingHandle function (evntrace.h)
description: Queries the system for the trace processing handle.helpviewer_keywords: ["QueryTraceProcessingHandle","QueryTraceProcessingHandle function [ETW]","etw.querytraceprocessinghandle","evntrace/QueryTraceProcessingHandle"]
old-location: etw\querytraceprocessinghandle.htm
tech.root: ETW
ms.assetid: 87666275-8752-4EC8-9C01-16D36AE4C5E8
ms.date: 12/05/2018
ms.keywords: QueryTraceProcessingHandle, QueryTraceProcessingHandle function [ETW], etw.querytraceprocessinghandle, evntrace/QueryTraceProcessingHandle
f1_keywords:
- evntrace/QueryTraceProcessingHandle
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# QueryTraceProcessingHandle function


## -description


Queries the system for the trace processing handle.


## -parameters




### -param ProcessingHandle [in]

A valid handle created with <a href="https://docs.microsoft.com/windows/desktop/ETW/opentrace">OpenTrace</a> that the data should be queried from.


### -param InformationClass [in]

An <a href="https://docs.microsoft.com/windows/desktop/ETW/etw-process-handle-info-type">ETW_PROCESS_HANDLE_INFO_TYPE</a> value that specifies what kind of operation will be done on the handle.


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
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>. 



