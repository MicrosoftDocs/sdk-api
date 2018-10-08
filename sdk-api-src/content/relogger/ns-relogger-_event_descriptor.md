---
UID: NS:relogger._EVENT_DESCRIPTOR
title: "_EVENT_DESCRIPTOR"
author: windows-sdk-content
description: Contains metadata that defines the event.
old-location: etw\event_descriptor.htm
tech.root: etw
ms.assetid: 907e6c38-5eaa-49da-9dc0-d055dcc69d1a
ms.author: windowssdkdev
ms.date: 10/04/2018
ms.keywords: "*PEVENT_DESCRIPTOR, EVENT_DESCRIPTOR, EVENT_DESCRIPTOR structure [ETW], PCEVENT_DESCRIPTOR, PCEVENT_DESCRIPTOR structure pointer [ETW], PEVENT_DESCRIPTOR, PEVENT_DESCRIPTOR structure pointer [ETW], _EVENT_DESCRIPTOR, base.event_descriptor, etw.event_descriptor, relogger/EVENT_DESCRIPTOR, relogger/PCEVENT_DESCRIPTOR, relogger/PEVENT_DESCRIPTOR"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: relogger.h
req.include-header: Evntprov.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - relogger.h
api_name:
 - EVENT_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: EVENT_DESCRIPTOR, *PEVENT_DESCRIPTOR
req.redist: 
---

# _EVENT_DESCRIPTOR structure


## -description


The <b>EVENT_DESCRIPTOR</b> structure contains metadata that defines the event.


## -struct-fields




### -field Id

The event identifier. 


### -field Version

The version of the event. The version indicates a revision to the event definition. You can use this member and the Id member to uniquely identify the event within the scope of a provider.


### -field Channel

The audience for the event (for example, administrator or developer). 


### -field Level

The severity or level of detail included in the event (for example, informational or fatal). 


### -field Opcode

A step in a sequence of operations being performed within the Task.


### -field Task

A larger unit of work within an application or component (is broader than the Opcode).


### -field Keyword

A bitmask that specifies a logical group of related events. Each bit corresponds to one group. An event may belong to one or more groups. The keyword can contain one or more provider-defined keywords, standard keywords, or both.


## -remarks



This structure represents an event defined in the manifest. You do not declare and populate this structure, instead you use the <a href="https://msdn.microsoft.com/f9de35f1-6d31-4f4b-b2c4-8474d6fce9e0">Message Compiler (MC.exe)</a> to generate a header file that declares and populates this structure for each event in the manifest. For details on writing the manifest and generating the header file, see <a href="https://msdn.microsoft.com/eec9d129-acde-4302-9121-634b3fad8455">Writing an Instrumentation Manifest</a> and <a href="https://msdn.microsoft.com/ecb72942-08fc-470d-b4d6-f5f1a70de3fa">Compiling an Instrumentation Manifest</a>.

For details on the members of this structure, see the attributes of the <a href="https://msdn.microsoft.com/09ea89c9-6618-4874-ac72-5ee19cde4040">EventDefinitionType</a> complex type. 

 You specify this structure when calling <a href="https://msdn.microsoft.com/93070eb7-c167-4419-abff-e861877dad07">EventWrite</a> or <a href="https://msdn.microsoft.com/798cf3ba-e1cc-4eaf-a1d2-2313a64aab1a">EventWriteTransfer</a> to write the event. You can also use it when calling <a href="https://msdn.microsoft.com/b332b6d4-6921-40bd-bebc-6646b5b9bcde">EventEnabled</a> to determine if you should write the event.

This structure is also included in the <a href="https://msdn.microsoft.com/479091ae-7229-433b-b93b-8da6cc18df89">EVENT_HEADER</a> structure that is returned with the event record when you consume events using the <a href="https://msdn.microsoft.com/80a30faf-af1f-4440-8a17-9df44bdb2291">EventRecordCallback</a> callback. For MOF-defined events, the <b>Opcode</b> member contains the event type value. The <b>Version</b> and <b>Level</b> members contain the expected information.




## -see-also




<a href="https://msdn.microsoft.com/479091ae-7229-433b-b93b-8da6cc18df89">EVENT_HEADER</a>



<a href="https://msdn.microsoft.com/05ce400e-c2e5-4852-9c41-d98ac2a6b467">EventDescCreate</a>



<a href="https://msdn.microsoft.com/193786ad-751e-477d-8747-a38b43292648">EventDescGetChannel</a>



<a href="https://msdn.microsoft.com/33deea6e-27e0-44ae-8d18-e8c854bc1819">EventDescGetId</a>



<a href="https://msdn.microsoft.com/4c96fad0-23c4-44cc-8b8f-2d62f08429d2">EventDescGetKeyword</a>



<a href="https://msdn.microsoft.com/29f356ad-c957-4a1e-abf8-5c7e6212c92e">EventDescGetLevel</a>



<a href="https://msdn.microsoft.com/cdca1dd8-da75-408c-9b57-0ac2bfe387b4">EventDescGetOpcode</a>



<a href="https://msdn.microsoft.com/5913587d-5c0d-4c50-99d9-8bff266b1c5b">EventDescGetTask</a>



<a href="https://msdn.microsoft.com/3881f089-d0c6-4d46-929a-09777df13f61">EventDescGetVersion</a>



<a href="https://msdn.microsoft.com/ad5e06cf-e2fa-4696-9521-61ff012b9204">EventDescOrKeyword</a>



<a href="https://msdn.microsoft.com/3580935d-ab7e-4409-b4ac-58f3c6019514">EventDescSetChannel</a>



<a href="https://msdn.microsoft.com/1c110ea3-651c-4e2c-9675-64f6975e5fc5">EventDescSetId</a>



<a href="https://msdn.microsoft.com/b1870a89-2e15-42b6-8441-82e6f9165540">EventDescSetKeyword</a>



<a href="https://msdn.microsoft.com/a4fe3b0e-6ca5-401c-a669-752e2955cc52">EventDescSetLevel</a>



<a href="https://msdn.microsoft.com/fe16eae0-5bff-4266-9b91-4b714540bde3">EventDescSetOpcode</a>



<a href="https://msdn.microsoft.com/74298e6f-b29a-4fa7-98d1-f81270fcbc0e">EventDescSetTask</a>



<a href="https://msdn.microsoft.com/f1d9fcb2-5a27-483b-b133-e8309b51165c">EventDescSetVersion</a>



<a href="https://msdn.microsoft.com/c52c5f6b-c7ab-47c2-8bce-55323bae7917">EventDescZero</a>



<a href="https://msdn.microsoft.com/b332b6d4-6921-40bd-bebc-6646b5b9bcde">EventEnabled</a>



<a href="https://msdn.microsoft.com/93070eb7-c167-4419-abff-e861877dad07">EventWrite</a>



<a href="https://msdn.microsoft.com/798cf3ba-e1cc-4eaf-a1d2-2313a64aab1a">EventWriteTransfer</a>



<a href="https://msdn.microsoft.com/CC392841-7436-4543-A846-FB5A27D9A014">PROVIDER_EVENT_INFO</a>



<a href="https://msdn.microsoft.com/93A03E1D-4047-49F1-987B-FB7BE03E0483">TdhEnumerateManifestProviderEvents</a>



<a href="https://msdn.microsoft.com/71702F1F-1708-4CA2-9BFB-3D7332AB6129">TdhGetManifestEventInformation</a>
 

 

