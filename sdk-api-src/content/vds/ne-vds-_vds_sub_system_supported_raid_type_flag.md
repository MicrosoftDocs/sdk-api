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

# _VDS_SUB_SYSTEM_SUPPORTED_RAID_TYPE_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of RAID levels that can be supported by subsystems.


## -enum-fields




### -field VDS_SF_SUPPORTS_RAID2_LUNS

Supports RAID level 2.


### -field VDS_SF_SUPPORTS_RAID3_LUNS

Supports RAID level 3.


### -field VDS_SF_SUPPORTS_RAID4_LUNS

Supports RAID level 4.


### -field VDS_SF_SUPPORTS_RAID5_LUNS

Supports RAID level 5.


### -field VDS_SF_SUPPORTS_RAID6_LUNS

Supports RAID level 6.


### -field VDS_SF_SUPPORTS_RAID01_LUNS

Supports RAID level 0+1.


### -field VDS_SF_SUPPORTS_RAID03_LUNS

Supports RAID level 0+3.


### -field VDS_SF_SUPPORTS_RAID05_LUNS

Supports RAID level 0+5.


### -field VDS_SF_SUPPORTS_RAID10_LUNS

Supports RAID level 1+0.


### -field VDS_SF_SUPPORTS_RAID15_LUNS

Supports RAID level 1+5.


### -field VDS_SF_SUPPORTS_RAID30_LUNS

Supports RAID level 3+0.


### -field VDS_SF_SUPPORTS_RAID50_LUNS

Supports RAID level 5+0.


### -field VDS_SF_SUPPORTS_RAID51_LUNS

Supports RAID level 5+1.


### -field VDS_SF_SUPPORTS_RAID53_LUNS

Supports RAID level 5+3.


### -field VDS_SF_SUPPORTS_RAID60_LUNS

Supports RAID level 6+0.


### -field VDS_SF_SUPPORTS_RAID61_LUNS

Supports RAID level 6+1.


## -remarks



The values of this enumeration are used in the <b>ulSupportedRaidTypeFlags</b> member of the <a href="https://msdn.microsoft.com/8eb743b5-26e6-42e5-b94b-0849b1280cdb">VDS_SUB_SYSTEM_PROP2</a> structure.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_SUB_SYSTEM_SUPPORTED_RAID_TYPE_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_SUB_SYSTEM_SUPPORTED_RAID_TYPE_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/7d19792c-cd37-4ea7-8830-c33c489e63e6">IVdsSubSystem2</a>



<a href="https://msdn.microsoft.com/1f2164a9-643d-4762-8a2e-31d5c277502e">IVdsSubSystem2::GetProperties2</a>



<a href="https://msdn.microsoft.com/c818d8f4-5ae5-4e40-91b9-a4405524066c">VDS_RAID_TYPE</a>



<a href="https://msdn.microsoft.com/8eb743b5-26e6-42e5-b94b-0849b1280cdb">VDS_SUB_SYSTEM_PROP2</a>
 

 

