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

# _VDS_SUB_SYSTEM_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the 
   properties of a <a href="https://msdn.microsoft.com/f605a5de-9256-4b43-8e12-3d78fd6cd9f1">subsystem object</a>.


## -struct-fields




### -field id

The GUID of the subsystem object.


### -field pwszFriendlyName

The name of the subsystem, typically a brand name and a model name; a zero-terminated, human-readable 
      string.


### -field pwszIdentification

The subsystem identifier; a zero-terminated, human-readable string.


### -field ulFlags

A bitmask of one or more   
      <a href="https://msdn.microsoft.com/17a07d21-a10a-4f18-a975-def6db073256">VDS_SUB_SYSTEM_FLAG</a> enumeration values.


### -field ulStripeSizeFlags

The set of stripe sizes supported by a provider for striped volumes and/or LUNs. A stripe size must be a 
      power of 2. Each bit in the 32-bit integer represents a size, in bytes. For example, if the <i>n</i>th 
      bit is set, then VDS supports stripe size of 2^<i>n</i>. Thus, bits 0 through 31 can specify 
      2^0 through 2^31.


### -field status

A <a href="https://msdn.microsoft.com/3393ff1f-df0f-4053-9127-d99196660f4b">VDS_SUB_SYSTEM_STATUS</a> enumeration value that specifies the status of the subsystem object.


### -field health

A 
      <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> enumeration value that specifies the health state of the subsystem. The following are the valid values for this member.



#### VDS_H_UNKNOWN (0)



#### VDS_H_HEALTHY (1)



#### VDS_H_FAILED (8)



#### VDS_H_DEGRADED (11)


### -field sNumberOfInternalBuses

The number of buses (or "channels") that the subsystem contains.


### -field sMaxNumberOfSlotsEachBus

The maximum number of slots that each of the buses can include. Each slot can accommodate one drive. The subsystem 
      model assumes that each bus has the same maximum number of slots.


### -field sMaxNumberOfControllers

The maximum number of controllers that the subsystem can contain.


### -field sRebuildPriority

The rebuild priority of the LUNs that belong to the subsystem. This value can range from 0 (lowest priority) through 15 (highest priority).


## -remarks



The <a href="https://msdn.microsoft.com/cbcf1e14-7e3d-44e6-8c4a-afe927ed0f9d">IVdsSubSystem::GetProperties</a> 
    method returns this structure to report the properties of a <a href="https://msdn.microsoft.com/f605a5de-9256-4b43-8e12-3d78fd6cd9f1">subsystem object</a>.




## -see-also




<a href="https://msdn.microsoft.com/cbcf1e14-7e3d-44e6-8c4a-afe927ed0f9d">IVdsSubSystem::GetProperties</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a>



<a href="https://msdn.microsoft.com/3393ff1f-df0f-4053-9127-d99196660f4b">VDS_SUB_SYSTEM_STATUS</a>
 

 

