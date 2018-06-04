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

# _VDS_STORAGE_POOL_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of <a href="https://msdn.microsoft.com/a6104742-3ef9-4570-9728-3e6580953117">storage pool</a> types. These values are used in the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">type</a> member of the <b>VDS_STORAGE_POOL_PROP</b> structure.


## -enum-fields




### -field VDS_SPT_UNKNOWN

The storage pool type is unknown.


### -field VDS_SPT_PRIMORDIAL

The storage pool type is primordial.


### -field VDS_SPT_CONCRETE

The storage pool type is concrete (non-primordial).


## -remarks



The terms <i>primordial storage pool</i> and <i>concrete storage pool</i> are defined in section 5.1.3 of the "Part 3: Block Devices" portion of the <a href=" http://go.microsoft.com/fwlink/p/?linkid=161225">SMI-S v1.5 specification</a>, which can be downloaded from the <a href="http://go.microsoft.com/fwlink/p/?linkid=161226">SNIA website</a>.

A storage area network (SAN) can contain one primordial pool. You can create multiple concrete pools within the primordial pool. The attributes in the <a href="https://msdn.microsoft.com/3dfbd3d9-ec2e-44ac-9d0f-7aa6c530db18">VDS_POOL_ATTRIBUTES</a> structure do not apply to a primordial pool, because it contains all physically available storage on the SAN. For example, suppose you have ten 10-GB SAN drives, five of which are in a concrete pool. In the Disk Management utility, the primordial pool has ten disk drives and a size of 100 GB, because it has a total of 100 GB of storage space available. The concrete pool has only 50 GB of storage space available. But if it is thin-provisioned, the size that the Disk Management utility reports for the concrete pool might be much larger than 50 GB.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_STORAGE_POOL_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_STORAGE_POOL_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2a82e872-2005-4b05-b67a-161b16c4f3aa">VDS_STORAGE_POOL_PROP</a>
 

 

