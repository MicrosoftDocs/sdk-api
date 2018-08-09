---
UID: NS:virtdisk._TAKE_SNAPSHOT_VHDSET_PARAMETERS
title: "_TAKE_SNAPSHOT_VHDSET_PARAMETERS"
author: windows-sdk-content
description: Contains snapshot parameters, indicating information about the new snapshot to be created.
old-location: vhd\take_snapshot_vhdset_parameters.htm
old-project: VStor
ms.assetid: 39D7287B-FA5E-4584-8E0A-69A857736D02
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PTAKE_SNAPSHOT_VHDSET_PARAMETERS, PTAKE_SNAPSHOT_VHDSET_PARAMETERS, PTAKE_SNAPSHOT_VHDSET_PARAMETERS structure pointer [VHD], TAKE_SNAPSHOT_VHDSET_PARAMETERS, TAKE_SNAPSHOT_VHDSET_PARAMETERS structure [VHD], _TAKE_SNAPSHOT_VHDSET_PARAMETERS, vdssys/PTAKE_SNAPSHOT_VHDSET_PARAMETERS, vdssys/TAKE_SNAPSHOT_VHDSET_PARAMETERS, vhd.take_snapshot_vhdset_parameters, virtdisk/PTAKE_SNAPSHOT_VHDSET_PARAMETERS, virtdisk/TAKE_SNAPSHOT_VHDSET_PARAMETERS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: virtdisk.h
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
req.typenames: TAKE_SNAPSHOT_VHDSET_PARAMETERS, *PTAKE_SNAPSHOT_VHDSET_PARAMETERS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
 - vdssys.h
api_name:
 - TAKE_SNAPSHOT_VHDSET_PARAMETERS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _TAKE_SNAPSHOT_VHDSET_PARAMETERS structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Contains snapshot parameters, indicating information about the new snapshot to be created. 



## -struct-fields




### -field Version

A value from the <a href="https://msdn.microsoft.com/E544AC22-6865-4ECF-92F8-B8027746C231">TAKE_SNAPSHOT_VHDSET_VERSION</a> enumeration that is the discriminant for the union. 



### -field Version1

A structure with the following member.


### -field Version1.SnapshotId

The Id of the new Snapshot to be added to the Vhd Set. 


