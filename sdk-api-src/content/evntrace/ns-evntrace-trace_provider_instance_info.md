---
UID: NS:evntrace._TRACE_PROVIDER_INSTANCE_INFO
title: TRACE_PROVIDER_INSTANCE_INFO (evntrace.h)
description: Defines an instance of the provider GUID.
old-location: etw\trace_provider_instance_info.htm
tech.root: ETW
ms.assetid: 49c11cd5-2cb1-474a-8b51-2d86b4501da1
ms.date: 12/05/2018
ms.keywords: '*PTRACE_PROVIDER_INSTANCE_INFO, PTRACE_PROVIDER_INSTANCE_INFO, PTRACE_PROVIDER_INSTANCE_INFO structure pointer [ETW], TRACE_PROVIDER_FLAG_LEGACY, TRACE_PROVIDER_FLAG_PRE_ENABLE, TRACE_PROVIDER_INSTANCE_INFO, TRACE_PROVIDER_INSTANCE_INFO structure [ETW], _TRACE_PROVIDER_INSTANCE_INFO, etw.trace_provider_instance_info, evntrace/PTRACE_PROVIDER_INSTANCE_INFO, evntrace/TRACE_PROVIDER_INSTANCE_INFO'
f1_keywords:
- evntrace/TRACE_PROVIDER_INSTANCE_INFO
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
- TRACE_PROVIDER_INSTANCE_INFO
targetos: Windows
req.typenames: TRACE_PROVIDER_INSTANCE_INFO, *PTRACE_PROVIDER_INSTANCE_INFO
req.redist: 
ms.custom: 19H1
---

# TRACE_PROVIDER_INSTANCE_INFO structure


## -description


Defines an instance of the provider GUID. 


## -struct-fields




### -field NextOffset

Offset, in bytes, from the beginning of this structure to the next <b>TRACE_PROVIDER_INSTANCE_INFO</b> structure. The value is zero if there is not another instance info block.


### -field EnableCount

Number of <a href="https://docs.microsoft.com/windows/desktop/ETW/trace-enable-info">TRACE_ENABLE_INFO</a> structures in this block. Each structure represents a session that enabled the provider.


### -field Pid

Process identifier of the process that registered the provider.


### -field Flags

Can be one of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRACE_PROVIDER_FLAG_LEGACY"></a><a id="trace_provider_flag_legacy"></a><dl>
<dt><b>TRACE_PROVIDER_FLAG_LEGACY</b></dt>
</dl>
</td>
<td width="60%">
The provider used <a href="https://docs.microsoft.com/windows/desktop/ETW/registertraceguids">RegisterTraceGuids</a> instead of <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventregister">EventRegister</a> to register itself. 

</td>
</tr>
<tr>
<td width="40%"><a id="TRACE_PROVIDER_FLAG_PRE_ENABLE"></a><a id="trace_provider_flag_pre_enable"></a><dl>
<dt><b>TRACE_PROVIDER_FLAG_PRE_ENABLE</b></dt>
</dl>
</td>
<td width="60%">
The provider is not registered; however, one or more sessions have enabled the provider.

</td>
</tr>
</table>
 


## -remarks



 If more than one provider uses the same GUID, the <a href="https://docs.microsoft.com/windows/desktop/ETW/trace-guid-info">TRACE_GUID_INFO</a> block contains more than one <b>TRACE_PROVIDER_INSTANCE_INFO</b> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/trace-enable-info">TRACE_ENABLE_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/trace-guid-info">TRACE_GUID_INFO</a>
 

 

