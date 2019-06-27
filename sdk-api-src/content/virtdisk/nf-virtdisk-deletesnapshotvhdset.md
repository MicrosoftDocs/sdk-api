---
UID: NF:virtdisk.DeleteSnapshotVhdSet
title: DeleteSnapshotVhdSet function (virtdisk.h)
author: windows-sdk-content
description: Deletes a snapshot from a VHD Set file.
old-location: vhd\deletesnapshotvhdset.htm
tech.root: VStor
ms.assetid: F6A65E00-857A-44CF-A827-747518564DAB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeleteSnapshotVhdSet, DeleteSnapshotVhdSet function [VHD], vdssys/DeleteSnapshotVhdSet, vhd.deletesnapshotvhdset, virtdisk/DeleteSnapshotVhdSet
ms.topic: function
f1_keywords: 
 - "virtdisk/DeleteSnapshotVhdSet"
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
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VirtDisk.dll
api_name:
 - DeleteSnapshotVhdSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DeleteSnapshotVhdSet function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Deletes a snapshot from a VHD Set file.


## -parameters




### -param VirtualDiskHandle [in]

A handle to the open virtual disk. This must be a VHD Set file.


### -param Parameters [in]

A pointer to a valid <a href="https://docs.microsoft.com/windows/desktop/api/vdssys/ns-vdssys-_delete_snapshot_vhdset_parameters">DELETE_SNAPSHOT_VHDSET_PARAMETERS</a> structure that contains snapshot deletion data.


### -param Flags [in]

Snapshot deletion flags, which must be a valid combination of the <a href="https://docs.microsoft.com/windows/desktop/api/vdssys/ne-vdssys-_delete_snapshot_vhdset_flag">DELETE_SNAPSHOT_VHDSET_FLAG</a> enumeration.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.



