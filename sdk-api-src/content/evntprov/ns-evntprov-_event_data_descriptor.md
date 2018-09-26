---
UID: NS:evntprov._EVENT_DATA_DESCRIPTOR
title: "_EVENT_DATA_DESCRIPTOR"
author: windows-sdk-content
description: The EVENT_DATA_DESCRIPTOR structure is used with the user mode EventWrite and the kernel mode EtwWrite functions to send events. The EVENT_DATA_DESCRIPTOR structure describes the event payload.
old-location: devtest\event_data_descriptor.htm
tech.root: devtest
ms.assetid: eb2b7ab6-52da-4d16-b315-6adab3131a05
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "*PEVENT_DATA_DESCRIPTOR, EVENT_DATA_DESCRIPTOR, EVENT_DATA_DESCRIPTOR structure [Driver Development Tools], Event Data Descriptor, Event Data Descriptor structure [Driver Development Tools], PEVENT_DATA_DESCRIPTOR, PEVENT_DATA_DESCRIPTOR structure pointer [Driver Development Tools], _EVENT_DATA_DESCRIPTOR, devtest.event_data_descriptor, etw_km_b9fc0f87-ef8a-43ef-aa07-33badda6ae53.xml, evntprov/EVENT_DATA_DESCRIPTOR, evntprov/PEVENT_DATA_DESCRIPTOR"
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
 - EVENT_DATA_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: EVENT_DATA_DESCRIPTOR, *PEVENT_DATA_DESCRIPTOR
req.redist: 
---

# _EVENT_DATA_DESCRIPTOR structure


## -description


The EVENT_DATA_DESCRIPTOR structure is used with the user mode <a href="http://go.microsoft.com/fwlink/p/?linkid=103400">EventWrite</a> and the kernel mode <a href="https://msdn.microsoft.com/b9d4f6da-694d-4737-9cbe-3666e693c0a2">EtwWrite</a> functions to send events. The EVENT_DATA_DESCRIPTOR structure describes the event payload. 


## -struct-fields




### -field Ptr

A pointer to the event descriptor data.


### -field Size

The size of the payload field, in bytes.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.Reserved

Reserved for future use.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Type

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Reserved1

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Reserved2

 




## -remarks



The most convenient method of populating the EVENT_DATA_DESCRIPTOR structure is to use the <b>EventDataDescCreate</b> macro. This macro is declared in Evntprov.h and its use is documented in the Microsoft Windows SDK documentation. The following example uses the <b>EventDataDescCreate</b> macro to populate an array of three EVENT_DATA_DESCRIPTOR structures. This array is then passed to the <b>EtwWrite</b> function. 


```
 EventDataDescCreate(&EventDataDescriptor[0],
                            (PVOID)&DeviceName.Length,
 sizeof(USHORT));

 EventDataDescCreate(&EventDataDescriptor[1],
                            (PVOID)DeviceName.Buffer,
 DeviceName.Length);
 
 EventDataDescCreate(&EventDataDescriptor[2],
                            (PVOID)&Status,
 sizeof(ULONG));
 
 EtwWrite(RegHandle,            // Handle from EtwRegister
                 &StartEvent,          // EventDescriptor
                 NULL,                 // Activity ID
                 3,                    // Number of data items
 EventDataDescriptor); // Array of data descriptors
    }              
```





## -see-also




<a href="https://msdn.microsoft.com/b9d4f6da-694d-4737-9cbe-3666e693c0a2">EtwWrite</a>



<a href="https://msdn.microsoft.com/cfe84b3d-fed2-4624-9899-8451e5b39de0">Event Descriptor</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=70404">EventDataDescCreate</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=103400">EventWrite</a>
 

 

