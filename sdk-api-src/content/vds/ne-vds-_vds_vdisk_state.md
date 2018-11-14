---
UID: NE:vds._VDS_VDISK_STATE
title: "_VDS_VDISK_STATE"
author: windows-sdk-content
description: Defines the set of status values for a virtual disk object.
old-location: base\vds_vdisk_state.htm
tech.root: VDS
ms.assetid: 62906f28-f6ae-488c-bf1f-655de5c7b95e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: VDS_VDISK_STATE, VDS_VDISK_STATE enumeration, VDS_VST_ADDED, VDS_VST_ATTACHED, VDS_VST_ATTACHED_NOT_OPEN, VDS_VST_ATTACH_PENDING, VDS_VST_COMPACTING, VDS_VST_DELETED, VDS_VST_DETACH_PENDING, VDS_VST_EXPANDING, VDS_VST_MAX, VDS_VST_MERGING, VDS_VST_OPEN, VDS_VST_UNKNOWN, _VDS_VDISK_STATE, base.vds_vdisk_state, vds/VDS_VDISK_STATE, vds/VDS_VST_ADDED, vds/VDS_VST_ATTACHED, vds/VDS_VST_ATTACHED_NOT_OPEN, vds/VDS_VST_ATTACH_PENDING, vds/VDS_VST_COMPACTING, vds/VDS_VST_DELETED, vds/VDS_VST_DETACH_PENDING, vds/VDS_VST_EXPANDING, vds/VDS_VST_MAX, vds/VDS_VST_MERGING, vds/VDS_VST_OPEN, vds/VDS_VST_UNKNOWN
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: vds.h
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
api_name:
 - VDS_VDISK_STATE
product: Windows
targetos: Windows
req.typenames: VDS_VDISK_STATE
req.redist: 
---

# _VDS_VDISK_STATE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of status values for a virtual disk object.


## -enum-fields




### -field VDS_VST_UNKNOWN

VDS was not able to identify the virtual disk's current status.


### -field VDS_VST_ADDED

The virtual disk is has been added to the VDS virtual disk provider.


### -field VDS_VST_OPEN

A handle has been opened to the virtual disk file.


### -field VDS_VST_ATTACH_PENDING

The virtual disk is being attached


### -field VDS_VST_ATTACHED_NOT_OPEN

The virtual disk is attached, but a handle has not been opened to the virtual disk file.


### -field VDS_VST_ATTACHED

The virtual disk is attached and a handle has  been opened to the virtual disk file.


### -field VDS_VST_DETACH_PENDING

The virtual disk is being detached and a handle is being opened to the virtual disk file.


### -field VDS_VST_COMPACTING

The virtual disk is being compacted.


### -field VDS_VST_MERGING

The virtual disk is being merged.


### -field VDS_VST_EXPANDING

The virtual disk is being expanded.


### -field VDS_VST_DELETED

The virtual disk has been deleted.


### -field VDS_VST_MAX

This value is reserved for system use.


## -remarks



<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_VDISK_STATE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_VDISK_STATE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>
 

 

