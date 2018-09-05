---
UID: NS:evntrace._TRACE_GUID_REGISTRATION
title: "_TRACE_GUID_REGISTRATION"
author: windows-sdk-content
description: The TRACE_GUID_REGISTRATION structure is used to register event trace classes.
old-location: etw\trace_guid_registration.htm
old-project: etw
ms.assetid: fc7b61fb-ef1c-48ec-8523-5f3114b5407a
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: "*PTRACE_GUID_REGISTRATION, TRACE_GUID_REGISTRATION, TRACE_GUID_REGISTRATION structure [ETW], _TRACE_GUID_REGISTRATION, _evt_trace_guid_registration, base.trace_guid_registration, etw.trace_guid_registration, evntrace/TRACE_GUID_REGISTRATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: evntrace.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: TRACE_GUID_REGISTRATION, *PTRACE_GUID_REGISTRATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evntrace.h
api_name:
 - TRACE_GUID_REGISTRATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _TRACE_GUID_REGISTRATION structure


## -description


The 
				<b>TRACE_GUID_REGISTRATION</b> structure is used to register event trace classes.
		


## -struct-fields




### -field Guid

Class GUID of an event trace class that you are registering.


### -field RegHandle

Handle to the registered event trace class. The <a href="https://msdn.microsoft.com/c9158292-281b-4a02-b280-956e340d225c">RegisterTraceGuids</a> function generates this value.

Use this handle when you call the <a href="https://msdn.microsoft.com/ab890392-f1e4-4b4e-a46c-8c7c2bfd3897">CreateTraceInstanceId</a> function and to set the <b>RegHandle</b> member of <a href="https://msdn.microsoft.com/2a79d937-2a3b-4426-b31f-a1a3ce86a334">EVENT_INSTANCE_HEADER</a> when calling the <a href="https://msdn.microsoft.com/e8361bdc-21dd-47a0-bdbf-56f4d6195689">TraceEventInstance</a> function.


## -remarks



Be sure to initialize the memory for this structure to zero before setting any members.




## -see-also




<a href="https://msdn.microsoft.com/ab890392-f1e4-4b4e-a46c-8c7c2bfd3897">CreateTraceInstanceId</a>



<a href="https://msdn.microsoft.com/c9158292-281b-4a02-b280-956e340d225c">RegisterTraceGuids</a>
 

 

