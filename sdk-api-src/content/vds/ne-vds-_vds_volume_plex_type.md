---
UID: NE:vds._VDS_VOLUME_PLEX_TYPE
title: "_VDS_VOLUME_PLEX_TYPE"
author: windows-sdk-content
description: Defines the set of valid types for a volume plex.
old-location: base\vds_volume_plex_type.htm
old-project: vds
ms.assetid: b0cd0418-35fa-40ff-964b-154c7f01f4df
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: VDS_VOLUME_PLEX_TYPE, VDS_VOLUME_PLEX_TYPE enumeration [VDS], VDS_VPT_PARITY, VDS_VPT_SIMPLE, VDS_VPT_SPAN, VDS_VPT_STRIPE, VDS_VPT_UNKNOWN, _VDS_VOLUME_PLEX_TYPE, base.vds_volume_plex_type, vds/VDS_VOLUME_PLEX_TYPE, vds/VDS_VPT_PARITY, vds/VDS_VPT_SIMPLE, vds/VDS_VPT_SPAN, vds/VDS_VPT_STRIPE, vds/VDS_VPT_UNKNOWN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: vds.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VDS_VOLUME_PLEX_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_VOLUME_PLEX_TYPE
product: Windows
targetos: Windows
req.lib: VdmDbg.lib
req.dll: VdmDbg.dll
req.irql: 
req.product: Windows UI
---

# _VDS_VOLUME_PLEX_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid types for a volume plex.


## -enum-fields




### -field VDS_VPT_UNKNOWN

This value is reserved.


### -field VDS_VPT_SIMPLE

The plex type is simple—it is composed of extents from exactly one disk. This value corresponds to the <b>VDS_VT_SIMPLE</b> value of the <a href="https://msdn.microsoft.com/07a44bbf-0726-4094-9b5f-2d26b0030796">VDS_VOLUME_TYPE</a> enumeration.


### -field VDS_VPT_SPAN

The plex type is spanned—it is composed of extents from more than one disk. This value corresponds to the <b>VDS_VT_SPAN</b> value of the <a href="https://msdn.microsoft.com/07a44bbf-0726-4094-9b5f-2d26b0030796">VDS_VOLUME_TYPE</a> enumeration.


### -field VDS_VPT_STRIPE

The plex type is striped, which is equivalent to RAID 0. This value corresponds to the <b>VDS_VT_STRIPE</b> value of the <a href="https://msdn.microsoft.com/07a44bbf-0726-4094-9b5f-2d26b0030796">VDS_VOLUME_TYPE</a> enumeration.


### -field VDS_VPT_PARITY

The plex type is striped with parity, which accounts for RAID levels 3, 4, 5, and 6. This value corresponds to the <b>VDS_VT_PARITY</b> value of the <a href="https://msdn.microsoft.com/07a44bbf-0726-4094-9b5f-2d26b0030796">VDS_VOLUME_TYPE</a> enumeration.


## -remarks



The <a href="https://msdn.microsoft.com/225cdc5e-045b-407f-b383-8f92025fbbd6">VDS_VOLUME_PLEX_PROP</a> structure includes a <b>VDS_VOLUME_PLEX_TYPE</b> value as a member to indicate the existing plex type.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_VOLUME_PLEX_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_VOLUME_PLEX_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/225cdc5e-045b-407f-b383-8f92025fbbd6">VDS_VOLUME_PLEX_PROP</a>



<a href="https://msdn.microsoft.com/07a44bbf-0726-4094-9b5f-2d26b0030796">VDS_VOLUME_TYPE</a>
 

 

