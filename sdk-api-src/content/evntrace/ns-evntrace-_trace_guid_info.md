---
UID: NS:evntrace._TRACE_GUID_INFO
title: "_TRACE_GUID_INFO"
author: windows-sdk-content
description: Defines the header to the list of sessions that enabled the provider specified in the InBuffer parameter of EnumerateTraceGuidsEx.
old-location: etw\trace_guid_info.htm
tech.root: etw
ms.assetid: 2c484adf-605d-420b-8059-942b35305acd
ms.author: windowssdkdev
ms.date: 10/04/2018
ms.keywords: "*PTRACE_GUID_INFO, PTRACE_GUID_INFO, PTRACE_GUID_INFO structure pointer [ETW], TRACE_GUID_INFO, TRACE_GUID_INFO structure [ETW], _TRACE_GUID_INFO, etw.trace_guid_info, evntrace/PTRACE_GUID_INFO, evntrace/TRACE_GUID_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - HeaderDef
api_location:
 - Evntrace.h
api_name:
 - TRACE_GUID_INFO
product: Windows
targetos: Windows
req.typenames: TRACE_GUID_INFO, *PTRACE_GUID_INFO
req.redist: 
---

# _TRACE_GUID_INFO structure


## -description


Defines the header to the list of sessions that enabled the provider specified in the <i>InBuffer</i> parameter of <a href="https://msdn.microsoft.com/9d70fe21-1750-4d60-a825-2004f7d666c7">EnumerateTraceGuidsEx</a>.


## -struct-fields




### -field InstanceCount

The number of <a href="https://msdn.microsoft.com/49c11cd5-2cb1-474a-8b51-2d86b4501da1">TRACE_PROVIDER_INSTANCE_INFO</a> blocks contained in the list. You can have multiple instances of the same provider if the provider lives in a DLL that is loaded by multiple processes.


### -field Reserved

Reserved.


## -remarks



Use the size of this structure to access the first <a href="https://msdn.microsoft.com/49c11cd5-2cb1-474a-8b51-2d86b4501da1">TRACE_PROVIDER_INSTANCE_INFO</a> block in the list.




## -see-also




<a href="https://msdn.microsoft.com/49c11cd5-2cb1-474a-8b51-2d86b4501da1">TRACE_PROVIDER_INSTANCE_INFO</a>
 

 

