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

# _VDS_VOLUME_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid types for a volume object.


## -enum-fields




### -field VDS_VT_UNKNOWN

The volume type is unknown.


### -field VDS_VT_SIMPLE

The volume type is simple—it is composed of extents from exactly one disk.


### -field VDS_VT_SPAN

The volume type is spanned—it is composed of extents from more than one disk.


### -field VDS_VT_STRIPE

The volume type is striped, which is equivalent to RAID 0.


### -field VDS_VT_MIRROR

The volume type is mirrored, which is equivalent to RAID 1.


### -field VDS_VT_PARITY

The volume type is striped with parity, which accounts for RAID levels 3, 4, 5, and 6.


## -remarks



The  <a href="https://msdn.microsoft.com/26fea1a4-f060-49e2-a7ac-0e751f798c72">IVdsPack::CreateVolume</a>
      method passes a <b>VDS_VOLUME_TYPE</b> value as an argument to set a new volume type, and the <a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a>
        structure includes a <b>VDS_VOLUME_TYPE</b> value as a member to indicate  the existing volume type.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_VOLUME_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_VOLUME_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/26fea1a4-f060-49e2-a7ac-0e751f798c72">
        IVdsPack::CreateVolume</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">
        VDS_VOLUME_PROP</a>
 

 

