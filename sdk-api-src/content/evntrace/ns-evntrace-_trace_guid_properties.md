---
UID: NS:evntrace._TRACE_GUID_PROPERTIES
title: "_TRACE_GUID_PROPERTIES"
author: windows-sdk-content
description: The TRACE_GUID_PROPERTIES structure contains information about an event trace provider.
old-location: etw\trace_guid_properties.htm
old-project: etw
ms.assetid: 849f2d34-14e0-43e8-a735-d46e94671725
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: "*PTRACE_GUID_PROPERTIES, PTRACE_GUID_PROPERTIES, PTRACE_GUID_PROPERTIES structure pointer [ETW], TRACE_GUID_PROPERTIES, TRACE_GUID_PROPERTIES structure [ETW], _TRACE_GUID_PROPERTIES, _evt_trace_guid_properties, base.trace_guid_properties, etw.trace_guid_properties, evntrace/PTRACE_GUID_PROPERTIES, evntrace/TRACE_GUID_PROPERTIES"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: evntrace.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: TRACE_GUID_PROPERTIES, *PTRACE_GUID_PROPERTIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evntrace.h
api_name:
 - TRACE_GUID_PROPERTIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _TRACE_GUID_PROPERTIES structure


## -description


The 
<b>TRACE_GUID_PROPERTIES</b> structure contains information about an event trace provider. 


## -struct-fields




### -field Guid

Control GUID of the event trace provider.


### -field GuidType

Not used.


### -field LoggerId

Session handle that identifies the event tracing session.


### -field EnableLevel

Value passed as the <i>EnableLevel</i> parameter to the 
<a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a> function.


### -field EnableFlags

Value passed as the <i>EnableFlag</i> parameter to the 
<a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a> function.


### -field IsEnable

If this member is <b>TRUE</b>, the element identified by the <b>Guid</b> member is currently enabled for the session identified by the <b>LoggerId</b> member. If this member is <b>FALSE</b>, all other members have no meaning and should be zero.


## -remarks



Be sure to initialize the memory for this structure to zero before setting any members or passing to any functions.




## -see-also




<a href="https://msdn.microsoft.com/9a9e2f53-9916-4a9c-a08e-c8affd5fc4c9">EnumerateTraceGuids</a>
 

 

