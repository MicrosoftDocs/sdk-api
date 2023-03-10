---
UID: NF:virtdisk.GetVirtualDiskOperationProgress
title: GetVirtualDiskOperationProgress function (virtdisk.h)
description: Checks the progress of an asynchronous virtual hard disk (VHD) operation.
helpviewer_keywords: ["GetVirtualDiskOperationProgress","GetVirtualDiskOperationProgress function [VHD]","vdssys/GetVirtualDiskOperationProgress","vhd.getvirtualdiskoperationprogress","virtdisk/GetVirtualDiskOperationProgress"]
old-location: vhd\getvirtualdiskoperationprogress.htm
tech.root: VStor
ms.assetid: 392a5258-306d-4c06-a632-85e6fc65ddc9
ms.date: 12/05/2018
ms.keywords: GetVirtualDiskOperationProgress, GetVirtualDiskOperationProgress function [VHD], vdssys/GetVirtualDiskOperationProgress, vhd.getvirtualdiskoperationprogress, virtdisk/GetVirtualDiskOperationProgress
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetVirtualDiskOperationProgress
 - virtdisk/GetVirtualDiskOperationProgress
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VirtDisk.dll
api_name:
 - GetVirtualDiskOperationProgress
---

# GetVirtualDiskOperationProgress function


## -description

Checks the progress of an asynchronous virtual hard disk (VHD) operation.

## -parameters

### -param VirtualDiskHandle [in]

A valid handle to a virtual disk with a pending asynchronous operation.

### -param Overlapped [in]

A pointer to a valid <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure. This 
     parameter must reference the same structure previously sent to the virtual disk operation being checked for 
     progress.

### -param Progress [out]

A pointer to a <a href="/windows/win32/api/virtdisk/ns-virtdisk-virtual_disk_progress">VIRTUAL_DISK_PROGRESS</a> 
     structure that receives the current virtual disk operation progress.

## -returns

Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b> and the 
      <i>Progress</i> parameter will be populated with the current virtual disk operation 
      progress.

If the function fails, the return value is an error code and the value of the 
      <i>Progress</i> parameter is undefined. For more information, see 
      <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>



<a href="/windows/win32/api/virtdisk/ns-virtdisk-virtual_disk_progress">VIRTUAL_DISK_PROGRESS</a>