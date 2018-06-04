---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

