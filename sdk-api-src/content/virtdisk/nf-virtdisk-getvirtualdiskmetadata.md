---
UID: NF:virtdisk.GetVirtualDiskMetadata
title: GetVirtualDiskMetadata function (virtdisk.h)
description: Retrieves the specified metadata from the virtual disk.
helpviewer_keywords: ["GetVirtualDiskMetadata","GetVirtualDiskMetadata function [Virtual Storage]","virtdisk/GetVirtualDiskMetadata","vstor.getvirtualdiskmetadata"]
old-location: vstor\getvirtualdiskmetadata.htm
tech.root: VStor
ms.assetid: 5dc5cf6e-c218-4aca-a574-499441bd1c12
ms.date: 12/05/2018
ms.keywords: GetVirtualDiskMetadata, GetVirtualDiskMetadata function [Virtual Storage], virtdisk/GetVirtualDiskMetadata, vstor.getvirtualdiskmetadata
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
 - GetVirtualDiskMetadata
 - virtdisk/GetVirtualDiskMetadata
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
 - GetVirtualDiskMetadata
---

# GetVirtualDiskMetadata function


## -description

Retrieves the specified metadata from the virtual disk.

## -parameters

### -param VirtualDiskHandle [in]

Handle to an open virtual disk.

### -param Item [in]

Address of a <b>GUID</b> identifying the metadata to retrieve.

### -param MetaDataSize [in, out]

Address of a <b>ULONG</b>. On input, the value indicates the size, in bytes, of 
      the buffer pointed to by the <i>MetaData</i> parameter. On output, the value contains size, 
      in bytes, of the retrieved metadata. If the buffer was too small, the API will fail and return 
      <b>ERROR_INSUFFICIENT_BUFFER</b>, putting the required size in the 
      <b>ULONG</b> and the buffer will contain the start of the metadata.

### -param MetaData [out]

Address of the buffer where the metadata is to be stored.

## -returns

Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the buffer pointed to by the <i>Items</i> parameter was too small, the return value is 
       <b>ERROR_INSUFFICIENT_BUFFER</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323699(v=vs.85)">VHD Functions</a>