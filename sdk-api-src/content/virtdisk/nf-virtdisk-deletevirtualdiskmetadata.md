---
UID: NF:virtdisk.DeleteVirtualDiskMetadata
title: DeleteVirtualDiskMetadata function (virtdisk.h)
description: Deletes metadata from a virtual disk.
helpviewer_keywords: ["DeleteVirtualDiskMetadata","DeleteVirtualDiskMetadata function [Virtual Storage]","virtdisk/DeleteVirtualDiskMetadata","vstor.deletevirtualdiskmetadata"]
old-location: vstor\deletevirtualdiskmetadata.htm
tech.root: VStor
ms.assetid: 16fbb793-84a9-4dac-a85e-0f4f50ae8e35
ms.date: 12/05/2018
ms.keywords: DeleteVirtualDiskMetadata, DeleteVirtualDiskMetadata function [Virtual Storage], virtdisk/DeleteVirtualDiskMetadata, vstor.deletevirtualdiskmetadata
req.header: virtdisk.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
 - DeleteVirtualDiskMetadata
 - virtdisk/DeleteVirtualDiskMetadata
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
 - DeleteVirtualDiskMetadata
---

# DeleteVirtualDiskMetadata function


## -description

Deletes metadata from a virtual disk.

## -parameters

### -param VirtualDiskHandle [in]

A handle to the open virtual disk.

### -param Item [in]

The item to be deleted.

## -returns

Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323699(v=vs.85)">VHD Functions</a>