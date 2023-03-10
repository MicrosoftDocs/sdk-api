---
UID: NF:virtdisk.SetVirtualDiskMetadata
title: SetVirtualDiskMetadata function (virtdisk.h)
description: Sets a metadata item for a virtual disk.
helpviewer_keywords: ["SetVirtualDiskMetadata","SetVirtualDiskMetadata function [Virtual Storage]","virtdisk/SetVirtualDiskMetadata","vstor.setvirtualdiskmetadata"]
old-location: vstor\setvirtualdiskmetadata.htm
tech.root: VStor
ms.assetid: 27ee1529-ccd9-43ea-aed9-4fd32d793354
ms.date: 12/05/2018
ms.keywords: SetVirtualDiskMetadata, SetVirtualDiskMetadata function [Virtual Storage], virtdisk/SetVirtualDiskMetadata, vstor.setvirtualdiskmetadata
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
 - SetVirtualDiskMetadata
 - virtdisk/SetVirtualDiskMetadata
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
 - SetVirtualDiskMetadata
---

# SetVirtualDiskMetadata function


## -description

Sets a metadata item for a virtual disk.

## -parameters

### -param VirtualDiskHandle [in]

Handle to an open virtual disk.

### -param Item [in]

Address of a <b>GUID</b> identifying the metadata to set. This cannot be the NULL GUID (a GUID of all zeroes).

### -param MetaDataSize [in]

Address of a <b>ULONG</b> containing the size, in bytes, of 
      the buffer pointed to by the <i>MetaData</i> parameter.
      Specific VHD file types have a maximum size per metadata element. Specific VHD files also have a maximum number of total metadata entries and total metadata size.

### -param MetaData [in]

Address of the buffer containing the metadata to be stored.

## -returns

Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323699(v=vs.85)">VHD Functions</a>
