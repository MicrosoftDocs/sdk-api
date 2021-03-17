---
UID: NF:virtdisk.ResizeVirtualDisk
title: ResizeVirtualDisk function (virtdisk.h)
description: Resizes a virtual disk.
helpviewer_keywords: ["ResizeVirtualDisk","ResizeVirtualDisk function [Virtual Storage]","virtdisk/ResizeVirtualDisk","vstor.resizevirtualdisk"]
old-location: vstor\resizevirtualdisk.htm
tech.root: VStor
ms.assetid: d000c03e-c0ad-4054-b2eb-1aca34a95816
ms.date: 12/05/2018
ms.keywords: ResizeVirtualDisk, ResizeVirtualDisk function [Virtual Storage], virtdisk/ResizeVirtualDisk, vstor.resizevirtualdisk
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
 - ResizeVirtualDisk
 - virtdisk/ResizeVirtualDisk
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
 - ResizeVirtualDisk
---

# ResizeVirtualDisk function


## -description

Resizes a virtual disk.

## -parameters

### -param VirtualDiskHandle [in]

Handle to an open virtual disk.

### -param Flags [in]

Zero or more flags enumerated from the 
      <a href="/windows/desktop/api/virtdisk/ne-virtdisk-resize_virtual_disk_flag">RESIZE_VIRTUAL_DISK_FLAG</a> enumeration.

### -param Parameters [in]

Address of a 
      <a href="/windows/desktop/api/virtdisk/ns-virtdisk-resize_virtual_disk_parameters">RESIZE_VIRTUAL_DISK_PARAMETERS</a> 
      structure containing the new size of the virtual disk.

### -param Overlapped [in, optional]

If this is to be an asynchronous operation, the address of a valid 
      <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure.

## -returns

Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/virtdisk/ne-virtdisk-resize_virtual_disk_flag">RESIZE_VIRTUAL_DISK_FLAG</a>



<a href="/windows/desktop/api/virtdisk/ns-virtdisk-resize_virtual_disk_parameters">RESIZE_VIRTUAL_DISK_PARAMETERS</a>



<a href="/previous-versions/windows/desktop/legacy/dd323699(v=vs.85)">VHD Functions</a>