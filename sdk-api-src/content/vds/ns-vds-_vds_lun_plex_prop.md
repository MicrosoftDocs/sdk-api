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

# _VDS_LUN_PLEX_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of a <a href="https://msdn.microsoft.com/db6eabaa-1b84-4613-ab2a-8d5904305e08">LUN plex object</a>.


## -struct-fields




### -field id

The GUID of the plex object. 


### -field ullSize

The size of the plex, in bytes. The size of the plex can be equal to or greater than that of the LUN to which the plex belongs. The plex cannot be smaller than the LUN.


### -field type

A <a href="https://msdn.microsoft.com/06aefde9-429b-4a58-923e-c3db6028eeb5">VDS_LUN_PLEX_TYPE</a> enumeration value that specifies the type of the plex. The type of the plex is not required to match the type of the LUN to which it belongs.


### -field status

A <a href="https://msdn.microsoft.com/04eed033-45b3-42bc-a304-25525cddd085">VDS_LUN_PLEX_STATUS</a> enumeration value that specifies the status of the plex. The status of the plex is not required to match the status of the LUN to which it belongs.


### -field health

<a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a>


#### VDS_H_UNKNOWN (0)



#### VDS_H_HEALTHY (1)



#### VDS_H_REBUILDING (2)



#### VDS_H_FAILING (4)



#### VDS_H_FAILING_REDUNDANCY (5)



#### VDS_H_FAILED_REDUNDANCY (6)



#### VDS_H_FAILED_REDUNDANCY_FAILING (7)



#### VDS_H_FAILED (8)


### -field TransitionState

A <a href="https://msdn.microsoft.com/ef688d1f-136b-4bc8-8209-e30033e752e9">VDS_TRANSITION_STATE</a> enumeration value that specifies the transition state of the plex.  The transition state of the plex is not required to match that of the LUN to which the plex belongs.


### -field ulFlags

A bitmask of <a href="https://msdn.microsoft.com/0258d87c-0270-449e-8e96-2c511c5f7242">VDS_LUN_PLEX_FLAG</a> enumeration values that describe the plex.


### -field ulStripeSize

The stripe interleave size, in bytes. This member is valid only for plexes of type <b>VDS_LPT_STRIPE</b> (striped) and <b>VDS_LPT_PARITY</b> (striped with parity). For other plex types, this member should be zero.


### -field sRebuildPriority

The rebuild priority of the plex. This value must be greater than or equal to 0 (lowest priority) and less than or equal to 15 (highest priority).


## -remarks



The <a href="https://msdn.microsoft.com/ded24edd-fa6a-48f3-a448-690078f034bb">IVdsLunPlex::GetProperties</a>
      method returns this structure to report the properties of a <a href="https://msdn.microsoft.com/db6eabaa-1b84-4613-ab2a-8d5904305e08">LUN plex object</a>.




## -see-also




<a href="https://msdn.microsoft.com/ded24edd-fa6a-48f3-a448-690078f034bb">IVdsLunPlex::GetProperties</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a>



<a href="https://msdn.microsoft.com/0258d87c-0270-449e-8e96-2c511c5f7242">VDS_LUN_PLEX_FLAG</a>



<a href="https://msdn.microsoft.com/04eed033-45b3-42bc-a304-25525cddd085">VDS_LUN_PLEX_STATUS</a>



<a href="https://msdn.microsoft.com/06aefde9-429b-4a58-923e-c3db6028eeb5">VDS_LUN_PLEX_TYPE</a>



<a href="https://msdn.microsoft.com/ef688d1f-136b-4bc8-8209-e30033e752e9">VDS_TRANSITION_STATE</a>
 

 

