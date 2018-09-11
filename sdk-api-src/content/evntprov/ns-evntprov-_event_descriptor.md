---
UID: NS:evntprov._EVENT_DESCRIPTOR
title: "_EVENT_DESCRIPTOR"
author: windows-sdk-content
description: The EVENT_DESCRIPTOR structure identifies the description information that is available for each event.
old-location: devtest\event_descriptor.htm
tech.root: devtest
ms.assetid: cfe84b3d-fed2-4624-9899-8451e5b39de0
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PEVENT_DESCRIPTOR, EVENT_DESCRIPTOR, EVENT_DESCRIPTOR structure [Driver Development Tools], Event Descriptor, Event Descriptor structure [Driver Development Tools], PEVENT_DESCRIPTOR, PEVENT_DESCRIPTOR structure pointer [Driver Development Tools], _EVENT_DESCRIPTOR, devtest.event_descriptor, etw_km_2dcb59a8-a21d-4520-8201-1074b9291978.xml, evntprov/EVENT_DESCRIPTOR, evntprov/PEVENT_DESCRIPTOR"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: evntprov.h
req.include-header: Wdm.h, Ntddk.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
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
 - evntprov.h
api_name:
 - EVENT_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: EVENT_DESCRIPTOR, *PEVENT_DESCRIPTOR
req.redist: 
---

# _EVENT_DESCRIPTOR structure


## -description


The EVENT_DESCRIPTOR structure identifies the description information that is available for each event. 


## -struct-fields




### -field Id

The event identifier. Each event is associated with a 16-bit numeric value. 


### -field Version

A numeric value that represents a version of the event. Component updates can change this value for a specific event.


### -field Channel

The channel that the event is intended for. Note that the channel name is not stored here. The value of the channel is assigned by the message compiler.


### -field Level

The level of the event. The level indicates the severity or verbosity of the event. The level is used  with earlier versions of the ETW and WPP event fields. The levels have names with values, such as Error, Warning, Information, and so on. 


### -field Opcode

The activity that the driver was performing at the time of the event. The <b>Opcode</b> member is defined by the provider or is one of the system-defined values defined in the Winmeta.xml file that is provided with the Windows Driver Kit (WDK) in the %Winddk%\<i>version</i>\inc\api directory.


### -field Task

The <b>Task</b> corresponds to the logical activity that the driver was performing when it raised the event. The <b>Opcode</b> member refers to a specific action within that logical activity.


### -field Keyword

The categories or tags assigned to the event. Each keyword categorizes the event in some way. For example, a category could be <b>Network</b>, <b>Storage</b>, or <b>Not Found</b>. An event can belong to more then one category, in which case multiple keywords are specified for the event. The keyword values are bitmasks and can be combined. 


## -remarks



The <b>Id</b> member is the event identifier. The structure members <b>Id</b> and <b>Version</b> can be used together to identify all events for a specific provider. When the <b>Id</b> and <b>Version</b> are used in conjunction with the manifest, you can precisely identify the structure and metadata of the event.

The pointer to the EVENT_DESCRIPTOR is passed to the <a href="https://msdn.microsoft.com/19aa5905-f611-46e2-8d70-a6cc4649c911">EtwEventEnabled</a>, <a href="https://msdn.microsoft.com/b9d4f6da-694d-4737-9cbe-3666e693c0a2">EtwWrite</a>, and <a href="https://msdn.microsoft.com/72a1c2f4-5f20-4c00-baf5-3d48fe27f48d">EtwWriteTransfer</a> functions. The most convenient method of populating the EVENT_DESCRIPTOR structure is to use the <b>EventDescCreate</b> macro. This macro is declared in Evntprov.h and its use is documented in the Microsoft Windows SDK. 

The following is a list of the convenience macros that you can use to create the event descriptors and to extract and set fields in the structure. For information on these macros, see <a href="http://go.microsoft.com/fwlink/p/?linkid=70405">Event Tracing Macros</a>.

<b>Macros to create event descriptors:
    </b>

<ul>
<li>
<b>EventDescCreate</b>

</li>
<li>
<b>EventDescZero</b>

</li>
</ul>
<b>Macros to extract information from an event descriptor:
    </b>

<ul>
<li>
<b>EventDescGetId</b>

</li>
<li>
<b>EventDescGetVersion</b>

</li>
<li>
<b>EventDescGetTask</b>

</li>
<li>
<b>EventDescGetOpcode</b>

</li>
<li>
<b>EventDescGetChannel</b>

</li>
<li>
<b>EventDescGetLevel</b>

</li>
<li>
<b>EventDescGetKeyword</b>

</li>
</ul>
<b>Macros to set fields in an event descriptor:</b>

<ul>
<li>
<b>EventDescSetId</b>

</li>
<li>
<b>EventDescSetVersion</b>

</li>
<li>
<b>EventDescSetTask</b>

</li>
<li>
<b>EventDescSetOpcode</b>

</li>
<li>
<b>EventDescSetLevel</b>

</li>
<li>
<b>EventDescSetChannel</b>

</li>
<li>
<b>EventDescSetKeyword</b>

</li>
<li>
<b>EventDescOrKeyword</b>

</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/b9d4f6da-694d-4737-9cbe-3666e693c0a2">EtwWrite</a>



<a href="https://msdn.microsoft.com/eb2b7ab6-52da-4d16-b315-6adab3131a05">Event Data Descriptor</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=70405">Event Tracing Macros</a>
 

 

