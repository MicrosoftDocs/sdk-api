---
UID: NS:evntrace._TRACE_ENABLE_INFO
title: "_TRACE_ENABLE_INFO"
author: windows-sdk-content
description: Defines the session and the information that the session used to enable the provider.
old-location: etw\trace_enable_info.htm
tech.root: ETW
ms.assetid: 999dd102-5937-4b1e-b841-623dddaa0df9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PTRACE_ENABLE_INFO, PTRACE_ENABLE_INFO, PTRACE_ENABLE_INFO structure pointer [ETW], TRACE_ENABLE_INFO, TRACE_ENABLE_INFO structure [ETW], _TRACE_ENABLE_INFO, etw.trace_enable_info, evntrace/PTRACE_ENABLE_INFO, evntrace/TRACE_ENABLE_INFO"
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
 - TRACE_ENABLE_INFO
product: Windows
targetos: Windows
req.typenames: TRACE_ENABLE_INFO, *PTRACE_ENABLE_INFO
req.redist: 
---

# _TRACE_ENABLE_INFO structure


## -description


Defines the session and the information that the session used to enable the provider.


## -struct-fields




### -field IsEnabled

Indicates if the provider is enabled to the session. The value is <b>TRUE</b> if the provider is enabled to the session, otherwise, the value is <b>FALSE</b>. This value should always be <b>TRUE</b>.


### -field Level

Level of detail that the session asked the provider to include in the events. For details, see the <i>Level</i> parameter of the <a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a> function.


### -field Reserved1

Reserved.


### -field LoggerId

Identifies the session that enabled the provider.


### -field EnableProperty

Additional information that the session wants ETW to include in the log file. For details, see the <i>EnableProperty</i> parameter of the <a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a> function.


### -field Reserved2

Reserved.


### -field MatchAnyKeyword

Keywords specify which events the session wants the provider to write. For details, see the <i>MatchAnyKeyword</i> parameter of the <a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a> function.


### -field MatchAllKeyword

Keywords specify which events the session wants the provider to write. For details, see the <i>MatchAllKeyword</i> parameter of the <a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a> function.


## -remarks



The <a href="https://msdn.microsoft.com/49c11cd5-2cb1-474a-8b51-2d86b4501da1">TRACE_PROVIDER_INSTANCE_INFO</a> block contains one or more of these structures.




## -see-also




<a href="https://msdn.microsoft.com/49c11cd5-2cb1-474a-8b51-2d86b4501da1">TRACE_PROVIDER_INSTANCE_INFO</a>
 

 

