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

# _VDS_DISK_EXTENT structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of 
   a disk extent.


## -struct-fields




### -field diskId

The GUID of the disk.


### -field type


      A <a href="https://msdn.microsoft.com/3f7a5dba-315b-4757-bd4c-1335c18739eb">VDS_DISK_EXTENT_TYPE</a> enumeration value that specifies the type of the disk extent.


### -field ullOffset

The disk offset, in bytes.


### -field ullSize

The size of the extent, in bytes.


### -field volumeId

The GUID of the volume to which the extent belongs.


### -field plexId

If the extent is from a volume, this member is the GUID of the plex to which the extent belongs.


### -field memberIdx

If the extent is from a volume plex, this member is the zero-based index of the plex member to which the extent belongs.


## -remarks




    The <i>volumeId</i>, <i>plexId</i>, and 
    <i>memberIdx</i> members apply to data and ESP partitions only. If the extent lacks a volume 
    association, the GUIDs for <i>volumeId</i> and <i>plexId</i> are GUID_NULL, 
    and <i>memberIdx</i> is zero. The <i>memberIdx</i> member is always zero 
    unless the volume is striped or striped with parity (RAID-5). An extent can also be unallocated or free.
   


    The <a href="https://msdn.microsoft.com/2e7de42f-da7a-41a7-b38e-849ab8d72ab2">IVdsDisk::QueryExtents</a> method returns this 
    structure to report the property details of a disk extent. Likewise, the 
    <a href="https://msdn.microsoft.com/09548bcc-29b9-498f-a4c0-99428f26343a">IVdsVolumePlex::QueryExtents</a> method 
    returns it to report the details of the disk extents allocated to a plex.


    A disk extent is a contiguous set of blocks on a single disk or LUN handled by a software provider. A drive 
    extent is not required to be a contiguous set of blocks.




## -see-also




<a href="https://msdn.microsoft.com/65e14273-8127-4667-b5c8-362ad54b4782">Disk Object</a>



<a href="https://msdn.microsoft.com/2e7de42f-da7a-41a7-b38e-849ab8d72ab2">IVdsDisk::QueryExtents</a>



<a href="https://msdn.microsoft.com/09548bcc-29b9-498f-a4c0-99428f26343a">IVdsVolumePlex::QueryExtents</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/3f7a5dba-315b-4757-bd4c-1335c18739eb">VDS_DISK_EXTENT_TYPE</a>
 

 

