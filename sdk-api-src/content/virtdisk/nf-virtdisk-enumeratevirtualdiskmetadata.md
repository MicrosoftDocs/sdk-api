---
UID: NF:virtdisk.EnumerateVirtualDiskMetadata
title: EnumerateVirtualDiskMetadata function (virtdisk.h)
description: Enumerates the metadata associated with a virtual disk.
helpviewer_keywords: ["EnumerateVirtualDiskMetadata","EnumerateVirtualDiskMetadata function [Virtual Storage]","virtdisk/EnumerateVirtualDiskMetadata","vstor.enumeratevirtualdiskmetadata"]
old-location: vstor\enumeratevirtualdiskmetadata.htm
tech.root: VStor
ms.assetid: 7817863a-38ca-4686-9d66-71700dba852f
ms.date: 12/05/2018
ms.keywords: EnumerateVirtualDiskMetadata, EnumerateVirtualDiskMetadata function [Virtual Storage], virtdisk/EnumerateVirtualDiskMetadata, vstor.enumeratevirtualdiskmetadata
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
 - EnumerateVirtualDiskMetadata
 - virtdisk/EnumerateVirtualDiskMetadata
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
 - EnumerateVirtualDiskMetadata
---

# EnumerateVirtualDiskMetadata function


## -description

Enumerates the metadata associated with a virtual disk.

## -parameters

### -param VirtualDiskHandle [in]

Handle to an open virtual disk.

### -param NumberOfItems [in, out]

Address of a <b>ULONG</b>. On input, the value indicates the number of elements in 
      the buffer pointed to by the <i>Items</i> parameter. On output, the value contains the number 
      of items retrieved. If the buffer was too small, the API will fail and return 
      <b>ERROR_INSUFFICIENT_BUFFER</b> and the <b>ULONG</b> will contain the 
      required buffer size.

### -param Items [out]

Address of a buffer to be filled with the <b>GUID</b>s representing the metadata. The 
      <a href="/windows/desktop/api/virtdisk/nf-virtdisk-getvirtualdiskmetadata">GetVirtualDiskMetadata</a> function can be used 
      to retrieve the data represented by each <b>GUID</b>.

## -returns

Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the buffer pointed to by the <i>Items</i> parameter was too small, the return value is 
       <b>ERROR_INSUFFICIENT_BUFFER</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323699(v=vs.85)">VHD Functions</a>