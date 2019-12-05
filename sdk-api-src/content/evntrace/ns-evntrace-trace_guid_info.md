---
UID: NS:evntrace._TRACE_GUID_INFO
title: TRACE_GUID_INFO (evntrace.h)
description: Defines the header to the list of sessions that enabled the provider specified in the InBuffer parameter of EnumerateTraceGuidsEx.
old-location: etw\trace_guid_info.htm
tech.root: ETW
ms.assetid: 2c484adf-605d-420b-8059-942b35305acd
ms.date: 12/05/2018
ms.keywords: '*PTRACE_GUID_INFO, PTRACE_GUID_INFO, PTRACE_GUID_INFO structure pointer [ETW], TRACE_GUID_INFO, TRACE_GUID_INFO structure [ETW], _TRACE_GUID_INFO, etw.trace_guid_info, evntrace/PTRACE_GUID_INFO, evntrace/TRACE_GUID_INFO'
ms.topic: struct
f1_keywords:
- evntrace/TRACE_GUID_INFO
dev_langs:
- c++
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
targetos: Windows
req.typenames: TRACE_GUID_INFO, *PTRACE_GUID_INFO
req.redist: 
ms.custom: 19H1
---

# TRACE_GUID_INFO structure


## -description


Defines the header to the list of sessions that enabled the provider specified in the <i>InBuffer</i> parameter of <a href="https://docs.microsoft.com/windows/desktop/ETW/enumeratetraceguidsex">EnumerateTraceGuidsEx</a>.


## -struct-fields




### -field InstanceCount

The number of <a href="https://docs.microsoft.com/windows/desktop/ETW/trace-provider-instance-info">TRACE_PROVIDER_INSTANCE_INFO</a> blocks contained in the list. You can have multiple instances of the same provider if the provider lives in a DLL that is loaded by multiple processes.


### -field Reserved

Reserved.


## -remarks



Use the size of this structure to access the first <a href="https://docs.microsoft.com/windows/desktop/ETW/trace-provider-instance-info">TRACE_PROVIDER_INSTANCE_INFO</a> block in the list.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/trace-provider-instance-info">TRACE_PROVIDER_INSTANCE_INFO</a>
 

 

