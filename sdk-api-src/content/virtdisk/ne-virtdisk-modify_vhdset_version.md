---
UID: NE:virtdisk._MODIFY_VHDSET_VERSION
title: MODIFY_VHDSET_VERSION (virtdisk.h)
author: windows-sdk-content
description: Contains the version of the MODIFY_VHDSET_PARAMETERS structure to use in calls to virtual disk functions.
old-location: vhd\modify_vhdset_version.htm
tech.root: VStor
ms.assetid: A93E73C9-63B2-49C3-A0E4-63BEC96F449A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PMODIFY_VHDSET_VERSION, MODIFY_VHDSET_DEFAULT_SNAPSHOT_PATH, MODIFY_VHDSET_REMOVE_SNAPSHOT, MODIFY_VHDSET_SNAPSHOT_PATH, MODIFY_VHDSET_UNSPECIFIED, MODIFY_VHDSET_VERSION, MODIFY_VHDSET_VERSION enumeration [VHD], PMODIFY_VHDSET_VERSION, PMODIFY_VHDSET_VERSION enumeration pointer [VHD], vdssys/MODIFY_VHDSET_DEFAULT_SNAPSHOT_PATH, vdssys/MODIFY_VHDSET_REMOVE_SNAPSHOT, vdssys/MODIFY_VHDSET_SNAPSHOT_PATH, vdssys/MODIFY_VHDSET_UNSPECIFIED, vdssys/MODIFY_VHDSET_VERSION, vdssys/PMODIFY_VHDSET_VERSION, vhd.modify_vhdset_version, virtdisk/MODIFY_VHDSET_DEFAULT_SNAPSHOT_PATH, virtdisk/MODIFY_VHDSET_REMOVE_SNAPSHOT, virtdisk/MODIFY_VHDSET_SNAPSHOT_PATH, virtdisk/MODIFY_VHDSET_UNSPECIFIED, virtdisk/MODIFY_VHDSET_VERSION, virtdisk/PMODIFY_VHDSET_VERSION"
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VirtDisk.h
 - vdssys.h
api_name:
 - MODIFY_VHDSET_VERSION
product: Windows
targetos: Windows
req.typenames: MODIFY_VHDSET_VERSION, *PMODIFY_VHDSET_VERSION
req.redist: 
ms.custom: 19H1
---

# MODIFY_VHDSET_VERSION enumeration


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Contains the version of the <a href="https://docs.microsoft.com/windows/desktop/api/vdssys/ns-vdssys-_modify_vhdset_parameters">MODIFY_VHDSET_PARAMETERS</a> structure to use in calls to virtual disk functions.


## -enum-fields




### -field MODIFY_VHDSET_UNSPECIFIED

Not Supported.


### -field MODIFY_VHDSET_SNAPSHOT_PATH

The <b>SnapshotPath</b> member structure will be used.


### -field MODIFY_VHDSET_REMOVE_SNAPSHOT

The <b>SnapshotId</b> member structure will be used.


### -field MODIFY_VHDSET_DEFAULT_SNAPSHOT_PATH

The <b>DefaultFilePath</b> member structure will be used

