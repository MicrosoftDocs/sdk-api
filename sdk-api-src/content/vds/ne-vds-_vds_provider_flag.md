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

# _VDS_PROVIDER_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set 
   of valid flags for a provider object.


## -enum-fields




### -field VDS_PF_DYNAMIC

The provider is a dynamic  provider. If this flag is set for the provider of a disk, the disk is dynamic.


### -field VDS_PF_INTERNAL_HARDWARE_PROVIDER

The operating system supplies this hardware provider to manage an internal hardware controller.


### -field VDS_PF_ONE_DISK_ONLY_PER_PACK

The provider supports single-disk packs only. Typically, the basic provider sets this flag to 
      simulate a pack with one disk.


### -field VDS_PF_ONE_PACK_ONLINE_ONLY

The provider is a dynamic provider that supports online status for only one pack at a time. 
     

<b>Windows Server 2003:  </b>Only applies to this release.


### -field VDS_PF_VOLUME_SPACE_MUST_BE_CONTIGUOUS

All volumes managed by this provider must have contiguous space. This flag applies to basic 
      providers only.


### -field VDS_PF_SUPPORT_DYNAMIC

If this flag is set, VDS sets the <b>VDS_SVF_SUPPORT_DYNAMIC</b> flag in the <a href="https://msdn.microsoft.com/9029ebbd-f05d-4317-913d-58c8a0a62886">VDS_SERVICE_PROP</a> structure.


### -field VDS_PF_SUPPORT_FAULT_TOLERANT

If this flag is set, VDS sets the <b>VDS_SVF_SUPPORT_FAULT_TOLERANT</b> 
      flag in the <a href="https://msdn.microsoft.com/9029ebbd-f05d-4317-913d-58c8a0a62886">VDS_SERVICE_PROP</a> structure.


### -field VDS_PF_SUPPORT_DYNAMIC_1394

If this flag is set, VDS sets the <b>VDS_SVF_SUPPORT_DYNAMIC_1394</b> 
      flag in the <a href="https://msdn.microsoft.com/9029ebbd-f05d-4317-913d-58c8a0a62886">VDS_SERVICE_PROP</a> structure.


### -field VDS_PF_SUPPORT_MIRROR

If this flag is set, VDS sets the <b>VDS_SVF_SUPPORT_MIRROR</b> flag in the <a href="https://msdn.microsoft.com/9029ebbd-f05d-4317-913d-58c8a0a62886">VDS_SERVICE_PROP</a> structure.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.


### -field VDS_PF_SUPPORT_RAID5

If this flag is set, VDS sets the <b>VDS_SVF_SUPPORT_RAID5</b> flag in the <a href="https://msdn.microsoft.com/9029ebbd-f05d-4317-913d-58c8a0a62886">VDS_SERVICE_PROP</a> structure.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.


## -remarks



This enumeration provides the values for the <i>ulFlags</i> member of the 
    <a href="https://msdn.microsoft.com/f41fc908-3720-4dfb-a5d3-bb1459fb7e5d">VDS_PROVIDER_PROP</a> structure.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_PROVIDER_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_PROVIDER_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/f41fc908-3720-4dfb-a5d3-bb1459fb7e5d">VDS_PROVIDER_PROP</a>
 

 

