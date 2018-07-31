---
UID: NS:vds._VDS_VOLUME_PLEX_PROP
title: "_VDS_VOLUME_PLEX_PROP"
author: windows-sdk-content
description: Defines the properties of a volume plex object.
old-location: base\vds_volume_plex_prop.htm
old-project: VDS
ms.assetid: 225cdc5e-045b-407f-b383-8f92025fbbd6
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PVDS_VOLUME_PLEX_PROP, PVDS_VOLUME_PLEX_PROP, PVDS_VOLUME_PLEX_PROP structure pointer [VDS], VDS_VOLUME_PLEX_PROP, VDS_VOLUME_PLEX_PROP structure [VDS], _VDS_VOLUME_PLEX_PROP, base.vds_volume_plex_prop, vds/PVDS_VOLUME_PLEX_PROP, vds/_VDS_VOLUME_PLEX_PROP"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: VDS_VOLUME_PLEX_PROP, *PVDS_VOLUME_PLEX_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_VOLUME_PLEX_PROP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_VOLUME_PLEX_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of a <a href="https://msdn.microsoft.com/9e770bfc-2bcb-45f0-a7fc-ba526349839e">volume plex object</a>.


## -struct-fields




### -field id

The GUID of the plex object.


### -field type

The plex type enumerated by <a href="https://msdn.microsoft.com/b0cd0418-35fa-40ff-964b-154c7f01f4df">VDS_VOLUME_PLEX_TYPE</a>. The type of the plex is not required to match the type of the volume to which the plex belongs.


### -field status

The status of the plex object enumerated by <a href="https://msdn.microsoft.com/2e382a68-876a-4287-a7df-d7eadd8ce037">VDS_VOLUME_PLEX_STATUS</a>. The status of the plex is not required to match the status of the volume to which the plex belongs.


### -field health

A  <a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a> enumeration value that specifies the health state of the plex.  The health state of the plex is not required to match the health state of the volume to which the plex belongs.


### -field TransitionState

A  <a href="https://msdn.microsoft.com/ef688d1f-136b-4bc8-8209-e30033e752e9">VDS_TRANSITION_STATE</a> enumeration value that specifies the transition state of the plex.


### -field ullSize

The size of the plex, in bytes. The size of the plex must be greater than or equal to that of the volume to which the plex belongs. The plex cannot be smaller than the volume.


### -field ulStripeSize

The stripe interleave size, in bytes. This member is valid only for plexes of type <b>VDS_VPT_STRIPE</b> (striped) and <b>VDS_VPT_PARITY</b> (striped with parity). For other plex types, this member should be zero.


### -field ulNumberOfMembers

The number of members in the volume plex. A plex member is a collection of concatenated disk extents contained on one more disks.


## -remarks



The <a href="https://msdn.microsoft.com/b5b6c141-3e9d-4e1a-9d3c-3c5063b3ab73">IVdsVolumePlex::GetProperties</a>method returns this structure to report the properties of a <a href="https://msdn.microsoft.com/9e770bfc-2bcb-45f0-a7fc-ba526349839e">volume plex object</a>.




## -see-also




<a href="https://msdn.microsoft.com/b5b6c141-3e9d-4e1a-9d3c-3c5063b3ab73">IVdsVolumePlex::GetProperties</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/c65d9266-d691-4711-8225-a442e90d8ba3">VDS_HEALTH</a>



<a href="https://msdn.microsoft.com/ef688d1f-136b-4bc8-8209-e30033e752e9">VDS_TRANSITION_STATE</a>



<a href="https://msdn.microsoft.com/2e382a68-876a-4287-a7df-d7eadd8ce037">VDS_VOLUME_PLEX_STATUS</a>



<a href="https://msdn.microsoft.com/b0cd0418-35fa-40ff-964b-154c7f01f4df">VDS_VOLUME_PLEX_TYPE</a>
 

 

