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
 

 

