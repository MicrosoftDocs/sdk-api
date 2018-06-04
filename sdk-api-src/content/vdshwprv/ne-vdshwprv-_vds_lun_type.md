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

# _VDS_LUN_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid types for a LUN.


## -enum-fields




### -field VDS_LT_UNKNOWN

This value is reserved.


### -field VDS_LT_DEFAULT

The LUN type is default automagic—the provider configures the LUN automatically based on hints. This value is used as an input parameter only; it is not returned by queries.


### -field VDS_LT_FAULT_TOLERANT

The LUN type is fault tolerant automagic—the provider configures the LUN automatically based on hints, but with the requirement that the resulting LUN is fault tolerant. This value is used as an input parameter only; it is not returned by queries.


### -field VDS_LT_NON_FAULT_TOLERANT

The LUN type is non-fault tolerant automagic—the provider configures the LUN automatically based on hints, but with the requirement that the resulting LUN is non-fault tolerant. This value is used as an input parameter only; it is not returned by queries.


### -field VDS_LT_SIMPLE

The LUN type is simple—it is composed of extents from exactly one drive.


### -field VDS_LT_SPAN

The LUN's type is spanned—it is composed of extents from more than one drive.


### -field VDS_LT_STRIPE

The LUN type is striped, which is equivalent to RAID 0.


### -field VDS_LT_MIRROR

The LUN type is mirrored, which is equivalent to RAID 1.


### -field VDS_LT_PARITY

The LUN type is striped with parity, which accounts for RAID levels 3, 4, 5, and 6.


### -field VDS_LT_RAID2

The LUN type is RAID level 2.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LT_RAID3

The LUN type is RAID level 3.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LT_RAID4

The LUN type is RAID level 4.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LT_RAID5

The LUN type is RAID level 5.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LT_RAID6

The LUN type is RAID level 6.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LT_RAID01

The LUN type is RAID level 0+1.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LT_RAID03

The LUN type is RAID level 0+3.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LT_RAID05

The LUN type is RAID level 0+5.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LT_RAID10

The LUN type is RAID level 1+0.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LT_RAID15

The LUN type is RAID level 1+5.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LT_RAID30

The LUN type is RAID level 3+0.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LT_RAID50

The LUN type is RAID level 5+0.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LT_RAID51

The LUN type is RAID level 5+1.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LT_RAID53

The LUN type is RAID level 5+3.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LT_RAID60

The LUN type is RAID level 6+0.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


### -field VDS_LT_RAID61

The LUN type is RAID level 6+1.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>This value is not supported.


## -remarks



The  
        <a href="https://msdn.microsoft.com/e8097364-1f23-4cda-8f12-a750bbb4eb4c">IVdsSubSystem::CreateLun</a> method passes a <b>VDS_LUN_TYPE</b> value as a parameter to set a new LUN type, and the <a href="https://msdn.microsoft.com/4ef0f4d8-7c63-4d8e-bf46-e6958661bd6a">VDS_LUN_PROP</a> structure includes a <b>VDS_LUN_TYPE</b> value as a member to indicate an existing LUN type.

If the <a href="https://msdn.microsoft.com/e8097364-1f23-4cda-8f12-a750bbb4eb4c">IVdsSubSystem::CreateLun</a> method returns a <b>VDS_LUN_TYPE</b> value that the caller does not recognize, the caller should display the LUN type as unknown. The caller should not attempt to map the unrecognized LUN type to another LUN type.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_LUN_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_LUN_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/1fa046dd-fac9-4246-a90b-1837206b164c">
        IVdsHwProviderStoragePools::CreateLunInStoragePool</a>



<b>
        IVdsSubSystem2::CreateLun2</b>



<a href="https://msdn.microsoft.com/e8097364-1f23-4cda-8f12-a750bbb4eb4c">
        IVdsSubSystem::CreateLun</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/4ef0f4d8-7c63-4d8e-bf46-e6958661bd6a">
        VDS_LUN_PROP</a>
 

 

