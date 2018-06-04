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

# _PERF_INSTANCE_DEFINITION structure


## -description


Describes an instance of a performance object.


## -struct-fields




### -field ByteLength

Size of this structure, including the instance name that follows, in bytes. This value must be an 8-byte multiple.


### -field ParentObjectTitleIndex

Index of the name of the parent object in the title database. For example, if the object is a thread, the parent object is a process, or if the object is a logical drive, the parent is a physical drive.


### -field ParentObjectInstance

Position of the instance within the parent object that is associated with this instance. The position is zero-based.


### -field UniqueID

A unique identifier that you can use to identify the instance instead of
                                        using the name to identify
                                        the instance. If you do not use unique identifiers to distinguish the counter instances, set this member to PERF_NO_UNIQUE_ID.


### -field NameOffset

Offset from the beginning of this structure to the Unicode name of this instance. 


### -field NameLength

Length of the instance name, including the null-terminator, in bytes. This member is zero if the instance does not have a name. 

Do not include in the length any padding that you added to the instance name to ensure that <b>ByteLength</b> is aligned to an 8-byte boundary. 


## -remarks



The object contains instances if the <b>NumInstances</b>  member of <a href="https://msdn.microsoft.com/9ed4f890-6256-45fd-a310-b5963a6131ae">PERF_OBJECT_TYPE</a> is greater than zero. Use the <b>DefinitionLength</b> member of <b>PERF_OBJECT_TYPE</b> to find the first instance of the object. For details, see <a href="https://msdn.microsoft.com/a68fa617-834c-4ad9-b922-fac3a648ad75">Performance Data Format</a>.

Consumers should use the parent instance name, if specified, to create a full instance name that is used for display. The convention is to form the name as parent/child.

Providers should use unique instance names. If you do not, it makes it difficult for consumers to calculate and display performance values because they cannot tell if the current instance refers to the same instance that was queried previously (instances can come and go). 

Providers must allocate enough space for the instance name to ensure that <b>ByteLength</b> is aligned to an 8-byte boundary. 




## -see-also




<a href="https://msdn.microsoft.com/9ed4f890-6256-45fd-a310-b5963a6131ae">PERF_OBJECT_TYPE</a>
 

 

