---
UID: NS:evntprov._EVENT_FILTER_HEADER
title: "_EVENT_FILTER_HEADER"
author: windows-sdk-content
description: Defines the header data that must precede the filter data that is defined in the instrumentation manifest.
old-location: etw\event_filter_header.htm
tech.root: etw
ms.assetid: 364a253d-f4c4-494a-af43-487c70912542
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PEVENT_FILTER_HEADER, EVENT_FILTER_HEADER, EVENT_FILTER_HEADER structure [ETW], PEVENT_FILTER_HEADER, PEVENT_FILTER_HEADER structure pointer [ETW], _EVENT_FILTER_HEADER, etw.event_filter_header, evntprov/EVENT_FILTER_HEADER, evntprov/PEVENT_FILTER_HEADER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: evntprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - Evntprov.h
api_name:
 - EVENT_FILTER_HEADER
product: Windows
targetos: Windows
req.typenames: EVENT_FILTER_HEADER, *PEVENT_FILTER_HEADER
req.redist: 
---

# _EVENT_FILTER_HEADER structure


## -description


Defines the header data that must precede the filter data that is defined in the instrumentation manifest.


## -struct-fields




### -field Id

The identifier that identifies the filter in the manifest for a schematized filter. The <b>value</b> attribute of the <b>filter</b> element contains the identifier.


### -field Version

The version number of the filter for a schematized filter. The <b>version</b> attribute of the <b>filter</b> element contains the version number.


### -field Reserved

Reserved


### -field InstanceId

An identifier that identifies the session that passed the filter. ETW sets this value; the session must set this member to zero. 

Providers use this value to set the <i>Filter</i> parameter of <a href="https://msdn.microsoft.com/00b907cb-45cd-48c7-bea4-4d8a39b4fa24">EventWriteEx</a> to prevent the event from being written to the session if the event data does not match the filter criteria (the provider determines the semantics of how the filter data is used in determining whether the event is written to the session).


### -field Size

The size, in bytes, of this header and the filter data that is appended to the end of this header.


### -field NextOffset

The offset from the beginning of this filter object to the next filter object. The value is zero if there are no more filter blocks. ETW sets this value; the session must set this member to zero. 


## -remarks



The filter data that you pass to the provider also includes a header. The following shows an example of how you would define a filter that contained three integers:

<pre class="syntax" xml:space="preserve"><code>struct _MY_FILTER {
    EVENT_FILTER_HEADER FilterHeader;
    ULONG Int1;
    ULONG Int2;
    ULONG Int3;
} MY_FILTER, *MY_FILTER;

MY_FILTER FilterData;
</code></pre>



## -see-also




<a href="https://msdn.microsoft.com/bc7cf886-f763-428a-9e75-031e8df26554">ENABLE_TRACE_PARAMETERS</a>



<a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a>



<a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a>



<a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a>
 

 

