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

# _VDS_VOLUME_STATUS enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of object status values for a volume.


## -enum-fields




### -field VDS_VS_UNKNOWN

The status of the volume is unknown. This value does not apply to dynamic volumes.


### -field VDS_VS_ONLINE

The volume is available.


### -field VDS_VS_NO_MEDIA

The volume is removable media, such as a CD-ROM.


### -field VDS_VS_FAILED

The volume is unavailable.


### -field VDS_VS_OFFLINE

The volume is offline.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported. If the volume is offline, the <b>VDS_VF_PERMANENTLY_DISMOUNTED</b> flag is set in the <b>ulFlags</b> member of the <a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a> or <a href="https://msdn.microsoft.com/e99aaead-f5ad-4181-9208-9158e9fac38f">VDS_VOLUME_PROP2</a> structure.


## -remarks



When the <a href="https://msdn.microsoft.com/0793642c-1905-470c-a69f-8bf5f8bbe90d">IVdsPack::GetProperties</a> method returns a <a href="https://msdn.microsoft.com/5d04bf6c-fda2-4b95-a8bb-907e64267f30">VDS_PACK_PROP</a> structure whose <b>status</b> member is VDS_PS_OFFLINE, VDS sets the status for all the  volumes in the pack to VDS_VS_FAILED. VDS sets the status for specific volume types to VDS_VS_FAILED under the following conditions:

<ul>
<li>For simple, spanned, and striped volumes—whenever a disk is missing.</li>
<li>For mirrored volumes—when any disk, except the last disk, is missing or has write errors that  the plex transitions to a detached condition. Likewise, if it is the last (non-stale) plex and the disk is missing.</li>
<li>For stripe with parity (RAID-5)—when the second disk is missing, or if one column becomes detached (because the disk is missing or the column has write errors), and a second disk is missing.</li>
</ul>
The <a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a>
      structure includes a <b>VDS_VOLUME_STATUS</b> value as a member to indicate the status of a volume.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_VOLUME_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_VOLUME_STATUS</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/5d04bf6c-fda2-4b95-a8bb-907e64267f30">VDS_PACK_PROP</a>



<a href="https://msdn.microsoft.com/a83d01e6-1173-410c-b880-3bc957d3f7e9">VDS_PACK_STATUS</a>



<a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">
        VDS_VOLUME_PROP</a>
 

 

