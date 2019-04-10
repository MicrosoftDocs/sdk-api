---
UID: NE:vdshwprv._VDS_RAID_TYPE
title: VDS_RAID_TYPE (vdshwprv.h)
author: windows-sdk-content
description: Defines the set enumeration values that can be used to specify the underlying RAID type of a storage pool.
old-location: base\vds_raid_type.htm
tech.root: VDS
ms.assetid: c818d8f4-5ae5-4e40-91b9-a4405524066c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PVDS_RAID_TYPE, VDS_RAID_TYPE, VDS_RAID_TYPE enumeration, VDS_RT_RAID0, VDS_RT_RAID01, VDS_RT_RAID03, VDS_RT_RAID05, VDS_RT_RAID1, VDS_RT_RAID10, VDS_RT_RAID15, VDS_RT_RAID2, VDS_RT_RAID3, VDS_RT_RAID30, VDS_RT_RAID4, VDS_RT_RAID5, VDS_RT_RAID50, VDS_RT_RAID51, VDS_RT_RAID53, VDS_RT_RAID6, VDS_RT_RAID60, VDS_RT_RAID61, VDS_RT_UNKNOWN, base.vds_raid_type, vds/VDS_RAID_TYPE, vds/VDS_RT_RAID0, vds/VDS_RT_RAID01, vds/VDS_RT_RAID03, vds/VDS_RT_RAID05, vds/VDS_RT_RAID1, vds/VDS_RT_RAID10, vds/VDS_RT_RAID15, vds/VDS_RT_RAID2, vds/VDS_RT_RAID3, vds/VDS_RT_RAID30, vds/VDS_RT_RAID4, vds/VDS_RT_RAID5, vds/VDS_RT_RAID50, vds/VDS_RT_RAID51, vds/VDS_RT_RAID53, vds/VDS_RT_RAID6, vds/VDS_RT_RAID60, vds/VDS_RT_RAID61, vds/VDS_RT_UNKNOWN, vdshwprv/VDS_RAID_TYPE, vdshwprv/VDS_RT_RAID0, vdshwprv/VDS_RT_RAID01, vdshwprv/VDS_RT_RAID03, vdshwprv/VDS_RT_RAID05, vdshwprv/VDS_RT_RAID1, vdshwprv/VDS_RT_RAID10, vdshwprv/VDS_RT_RAID15, vdshwprv/VDS_RT_RAID2, vdshwprv/VDS_RT_RAID3, vdshwprv/VDS_RT_RAID30, vdshwprv/VDS_RT_RAID4, vdshwprv/VDS_RT_RAID5, vdshwprv/VDS_RT_RAID50, vdshwprv/VDS_RT_RAID51, vdshwprv/VDS_RT_RAID53, vdshwprv/VDS_RT_RAID6, vdshwprv/VDS_RT_RAID60, vdshwprv/VDS_RT_RAID61, vdshwprv/VDS_RT_UNKNOWN"
ms.topic: enum
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_RAID_TYPE
product: Windows
targetos: Windows
req.typenames: VDS_RAID_TYPE, *PVDS_RAID_TYPE
req.redist: 
---

# VDS_RAID_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set enumeration values that can be used to specify the underlying RAID type of a  <a href="https://msdn.microsoft.com/a6104742-3ef9-4570-9728-3e6580953117">storage pool</a>. These values are used in the <b>raidType</b> member of the <a href="https://msdn.microsoft.com/3dfbd3d9-ec2e-44ac-9d0f-7aa6c530db18">VDS_POOL_ATTRIBUTES</a> structure.


## -enum-fields




### -field VDS_RT_UNKNOWN

The RAID level is unknown.


### -field VDS_RT_RAID0

RAID level 0.


### -field VDS_RT_RAID1

RAID level 1.


### -field VDS_RT_RAID2

RAID level 2.


### -field VDS_RT_RAID3

RAID level 3.


### -field VDS_RT_RAID4

RAID level 4.


### -field VDS_RT_RAID5

RAID level 5.


### -field VDS_RT_RAID6

RAID level 6.


### -field VDS_RT_RAID01

RAID level 0+1.


### -field VDS_RT_RAID03

RAID level 0+3.


### -field VDS_RT_RAID05

RAID level 0+5.


### -field VDS_RT_RAID10

RAID level 1+0.


### -field VDS_RT_RAID15

RAID level 1+5.


### -field VDS_RT_RAID30

RAID level 3+0.


### -field VDS_RT_RAID50

RAID level 5+0.


### -field VDS_RT_RAID51

RAID level 5+1.


### -field VDS_RT_RAID53

RAID level 5+3.


### -field VDS_RT_RAID60

RAID level 6+0.


### -field VDS_RT_RAID61

RAID level 6+1.


## -remarks



A subsystem uses a  <b>VDS_RAID_TYPE</b> enumeration value to specify the underlying RAID type of a storage pool. 

A storage pool does not necessarily have a single underlying RAID type. For example, 

The underlying RAID type of of the storage pool is different from the RAID type of a LUN that can be created from the storage pool.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_RAID_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_RAID_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/3dfbd3d9-ec2e-44ac-9d0f-7aa6c530db18">VDS_POOL_ATTRIBUTES</a>
 

 

