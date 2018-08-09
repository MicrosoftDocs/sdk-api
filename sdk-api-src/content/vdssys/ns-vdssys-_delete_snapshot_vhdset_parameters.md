---
UID: NS:vdssys._DELETE_SNAPSHOT_VHDSET_PARAMETERS
title: "_DELETE_SNAPSHOT_VHDSET_PARAMETERS"
author: windows-sdk-content
description: Contains snapshot deletion parameters, designating which snapshot to delete from the VHD Set.
old-location: vhd\delete_snapshot_vhdset_parameters.htm
old-project: VStor
ms.assetid: A10EB006-2FE5-4445-9E2F-DF2C1AF0A44F
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PDELETE_SNAPSHOT_VHDSET_PARAMETERS, DELETE_SNAPSHOT_VHDSET_PARAMETERS, DELETE_SNAPSHOT_VHDSET_PARAMETERS structure [VHD], PDELETE_SNAPSHOT_VHDSET_PARAMETERS, PDELETE_SNAPSHOT_VHDSET_PARAMETERS structure pointer [VHD], _DELETE_SNAPSHOT_VHDSET_PARAMETERS, vdssys/DELETE_SNAPSHOT_VHDSET_PARAMETERS, vdssys/PDELETE_SNAPSHOT_VHDSET_PARAMETERS, vhd.delete_snapshot_vhdset_parameters, virtdisk/DELETE_SNAPSHOT_VHDSET_PARAMETERS, virtdisk/PDELETE_SNAPSHOT_VHDSET_PARAMETERS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vdssys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: DELETE_SNAPSHOT_VHDSET_PARAMETERS, *PDELETE_SNAPSHOT_VHDSET_PARAMETERS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
 - vdssys.h
api_name:
 - DELETE_SNAPSHOT_VHDSET_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _DELETE_SNAPSHOT_VHDSET_PARAMETERS structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Contains snapshot deletion parameters, designating which snapshot to delete from the VHD Set.


## -struct-fields




### -field Version

A value from the <a href="https://msdn.microsoft.com/D92039E2-775F-4A77-83AA-5681A1A67835">DELETE_SNAPSHOT_VHDSET_VERSION</a> enumeration that is the discriminant for the union.


### -field Version1

A structure with the following member.


### -field Version1.SnapshotId

The Snapshot Id in GUID format indicating which snapshot is to be deleted from the VHD Set. 


