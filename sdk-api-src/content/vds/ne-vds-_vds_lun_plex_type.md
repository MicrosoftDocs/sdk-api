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

# _VDS_LUN_PLEX_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid types for a LUN plex.


## -enum-fields




### -field VDS_LPT_UNKNOWN

This value is reserved.


### -field VDS_LPT_SIMPLE

The plex type is simple—it is composed of extents from exactly one drive.


### -field VDS_LPT_SPAN

The plex type is spanned—it is composed of extents from more than one drive.


### -field VDS_LPT_STRIPE

The plex type is striped, which is equivalent to RAID 0.


### -field VDS_LPT_PARITY

The plex type is striped with parity, which accounts for RAID levels 3, 4, 5, and 6.


### -field VDS_LPT_RAID2

The plex type is RAID level 2.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LPT_RAID3

The plex type is RAID level 3.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LPT_RAID4

The plex type is RAID level 4.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LPT_RAID5

The plex type is RAID level 5.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LPT_RAID6

The plex type is RAID level 6.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LPT_RAID03

The plex type is RAID level 0+3.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LPT_RAID05

The plex type is RAID level 0+5.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LPT_RAID10

The plex type is RAID level 1+0.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LPT_RAID15

The plex type is RAID level 1+5.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LPT_RAID30

The plex type is RAID level 3+0.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LPT_RAID50

The plex type is RAID level 5+0.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LPT_RAID53

The plex type is RAID level 5+3.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LPT_RAID60

The plex type is RAID level 6+0.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


## -remarks



The  <a href="https://msdn.microsoft.com/d79ce5a9-af5a-4691-b853-c18d4a4d04c7">VDS_LUN_PLEX_PROP</a>
       structure includes a <b>VDS_LUN_PLEX_TYPE</b> value as a member to indicate the existing plex type.

If your application encounters a <a href="https://msdn.microsoft.com/b16cc14b-4aef-43ec-9232-a95de06f1194">VDS_HWPROVIDER_TYPE</a> value that it does not recognize, it should display the provider type as unknown. It should not attempt to map the unrecognized provider type to another provider type.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_LUN_PLEX_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_LUN_PLEX_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/d79ce5a9-af5a-4691-b853-c18d4a4d04c7">
        VDS_LUN_PLEX_PROP</a>



<a href="https://msdn.microsoft.com/0952db7d-9dd6-4602-82d4-66d773c14463">VDS_LUN_TYPE</a>
 

 

