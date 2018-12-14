---
UID: NS:evntprov._EVENT_FILTER_DESCRIPTOR
title: EVENT_FILTER_DESCRIPTOR
author: windows-sdk-content
description: The EVENT_FILTER_DESCRIPTOR structure supplements the event provider, level, and keyword data that determines which events are reported and traced.
old-location: devtest\event_filter_descriptor.htm
tech.root: devtest
ms.assetid: 3870a471-a3cf-424f-bba3-bc06de1ebecc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PEVENT_FILTER_DESCRIPTOR, EVENT_FILTER_DESCRIPTOR, EVENT_FILTER_DESCRIPTOR structure [Driver Development Tools], Event Filter Descriptor, Event Filter Descriptor structure [Driver Development Tools], PEVENT_FILTER_DESCRIPTOR, PEVENT_FILTER_DESCRIPTOR structure pointer [Driver Development Tools], devtest.event_filter_descriptor, etw_km_a59972ec-314f-456d-98c3-5fe39445effe.xml, evntprov/EVENT_FILTER_DESCRIPTOR, evntprov/PEVENT_FILTER_DESCRIPTOR"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - EVENT_FILTER_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: EVENT_FILTER_DESCRIPTOR, *PEVENT_FILTER_DESCRIPTOR
req.redist: 
---

# EVENT_FILTER_DESCRIPTOR structure


## -description


The EVENT_FILTER_DESCRIPTOR structure supplements the event provider, level, and keyword data that determines which events are reported and traced. The EVENT_FILTER_DESCRIPTOR structure gives the event provider greater control over the selection of events for reporting and tracing. 


## -struct-fields




### -field Ptr

A pointer to the filter data. 


### -field Size

The size of the filter data, in bytes. The maximum size is 1024 bytes.


### -field Type

The type of filter data. The type is application-defined. An event controller  that knows about the provider and knows details about the provider's events can use the <b>Type</b> field to send the provider an arbitrary set of data for use as enhancements to the filtering of events.


## -remarks



You pass a pointer to the EVENT_FILTER_DESCRIPTOR structure when you create the optional driver-supplied <a href="https://msdn.microsoft.com/5953a3ae-b130-42fd-9dc8-974d15c6dfc5">EtwEnableCallback</a>function. When you register the driver with ETW, the <a href="https://msdn.microsoft.com/89a37edb-0f58-45c2-9045-b31eec5a4281">EtwRegister</a> function takes a pointer to the <b>EtwEnableCallback</b> function as a parameter.




## -see-also




<a href="https://msdn.microsoft.com/5953a3ae-b130-42fd-9dc8-974d15c6dfc5">EtwEnableCallback</a>



<a href="https://msdn.microsoft.com/89a37edb-0f58-45c2-9045-b31eec5a4281">EtwRegister</a>
 

 

