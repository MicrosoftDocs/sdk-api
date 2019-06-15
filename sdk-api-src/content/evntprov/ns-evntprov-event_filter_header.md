---
UID: NS:evntprov._EVENT_FILTER_HEADER
title: EVENT_FILTER_HEADER (evntprov.h)
author: windows-sdk-content
description: Defines the header data that must precede the filter data that is defined in the instrumentation manifest.
old-location: etw\event_filter_header.htm
tech.root: ETW
ms.assetid: 364a253d-f4c4-494a-af43-487c70912542
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PEVENT_FILTER_HEADER, EVENT_FILTER_HEADER, EVENT_FILTER_HEADER structure [ETW], PEVENT_FILTER_HEADER, PEVENT_FILTER_HEADER structure pointer [ETW], etw.event_filter_header, evntprov/EVENT_FILTER_HEADER, evntprov/PEVENT_FILTER_HEADER"
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
ms.custom: 19H1
---

# EVENT_FILTER_HEADER structure


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

Providers use this value to set the <i>Filter</i> parameter of <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventwriteex">EventWriteEx</a> to prevent the event from being written to the session if the event data does not match the filter criteria (the provider determines the semantics of how the filter data is used in determining whether the event is written to the session).


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




<a href="https://docs.microsoft.com/windows/desktop/ETW/enable-trace-parameters">ENABLE_TRACE_PARAMETERS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-_event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/enabletrace">EnableTrace</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex-func">EnableTraceEx</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a>
 

 

