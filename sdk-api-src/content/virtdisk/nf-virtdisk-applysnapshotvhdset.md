---
UID: NF:virtdisk.ApplySnapshotVhdSet
title: ApplySnapshotVhdSet function (virtdisk.h)
author: windows-sdk-content
description: Applies a snapshot of the current virtual disk for VHD Set files.
old-location: vhd\applysnapshotvhdset.htm
tech.root: VStor
ms.assetid: 1194B20E-AA50-4AEC-B9C4-AEA1BA84DD99
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ApplySnapshotVhdSet, ApplySnapshotVhdSet function [VHD], vdssys/ApplySnapshotVhdSet, vhd.applysnapshotvhdset, virtdisk/ApplySnapshotVhdSet
ms.topic: function
f1_keywords: 
 - "virtdisk/ApplySnapshotVhdSet"
dev_langs:
 - c++
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - ApplySnapshotVhdSet
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ApplySnapshotVhdSet function


## -description


Applies a snapshot of the current virtual disk for VHD Set files.


## -parameters




### -param VirtualDiskHandle [in]

A handle to an open virtual disk. For information on how to open a virtual disk, see the 
      <a href="https://docs.microsoft.com/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a> function.


### -param Parameters [in]

A pointer to a valid <a href="https://docs.microsoft.com/windows/win32/api/virtdisk/ns-virtdisk-apply_snapshot_vhdset_parameters">APPLY_SNAPSHOT_VHDSET_PARAMETERS</a> structure that contains snapshot data.


### -param Flags [in]

A valid combination of values of the 
      <a href="https://docs.microsoft.com/windows/win32/api/virtdisk/ne-virtdisk-apply_snapshot_vhdset_flag">APPLY_SNAPSHOT_VHDSET_FLAG</a> enumeration.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd323699(v=vs.85)">VHD Functions</a>
 

 

