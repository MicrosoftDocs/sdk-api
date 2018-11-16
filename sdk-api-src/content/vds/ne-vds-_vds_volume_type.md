---
UID: NE:vds._VDS_VOLUME_TYPE
title: "_VDS_VOLUME_TYPE"
author: windows-sdk-content
description: Defines the set of valid types for a volume object.
old-location: base\vds_volume_type.htm
tech.root: VDS
ms.assetid: 07a44bbf-0726-4094-9b5f-2d26b0030796
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: VDS_VOLUME_TYPE, VDS_VOLUME_TYPE enumeration [VDS], VDS_VT_MIRROR, VDS_VT_PARITY, VDS_VT_SIMPLE, VDS_VT_SPAN, VDS_VT_STRIPE, VDS_VT_UNKNOWN, _VDS_VOLUME_TYPE, base.vds_volume_type, vds/VDS_VOLUME_TYPE, vds/VDS_VT_MIRROR, vds/VDS_VT_PARITY, vds/VDS_VT_SIMPLE, vds/VDS_VT_SPAN, vds/VDS_VT_STRIPE, vds/VDS_VT_UNKNOWN
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
api_name:
 - VDS_VOLUME_TYPE
product: Windows
targetos: Windows
req.typenames: VDS_VOLUME_TYPE
req.redist: 
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



The  <a href="https://msdn.microsoft.com/26fea1a4-f060-49e2-a7ac-0e751f798c72">IVdsPack::CreateVolume</a>method passes a <b>VDS_VOLUME_TYPE</b> value as an argument to set a new volume type, and the <a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a>structure includes a <b>VDS_VOLUME_TYPE</b> value as a member to indicate  the existing volume type.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_VOLUME_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_VOLUME_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/26fea1a4-f060-49e2-a7ac-0e751f798c72">IVdsPack::CreateVolume</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">VDS_VOLUME_PROP</a>
 

 

