---
UID: NF:virtdisk.GetStorageDependencyInformation
title: GetStorageDependencyInformation function (virtdisk.h)
description: Returns the relationships between virtual hard disks (VHDs) or CD or DVD image file (ISO) or the volumes contained within those disks and their parent disk or volume.
helpviewer_keywords: ["GetStorageDependencyInformation","GetStorageDependencyInformation function [VHD]","vdssys/GetStorageDependencyInformation","vhd.getstoragedependencyinformation","virtdisk/GetStorageDependencyInformation"]
old-location: vhd\getstoragedependencyinformation.htm
tech.root: VStor
ms.assetid: 9ed3ec7c-5e50-4e81-bba7-798f2fbcf29d
ms.date: 12/05/2018
ms.keywords: GetStorageDependencyInformation, GetStorageDependencyInformation function [VHD], vdssys/GetStorageDependencyInformation, vhd.getstoragedependencyinformation, virtdisk/GetStorageDependencyInformation
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
 - GetStorageDependencyInformation
 - virtdisk/GetStorageDependencyInformation
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
 - GetStorageDependencyInformation
---

# GetStorageDependencyInformation function


## -description

Returns the relationships between virtual hard disks (VHDs) or CD or DVD image file (ISO) or the 
    volumes contained within those disks and their parent disk or volume.

## -parameters

### -param ObjectHandle [in]

A handle to a volume or root directory if  the <i>Flags</i> parameter does not specify 
      the <b>GET_STORAGE_DEPENDENCY_FLAG_DISK_HANDLE</b> flag. For information on how to open a 
      volume or root directory, see the <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

If the <i>Flags</i> parameter specifies the 
      <b>GET_STORAGE_DEPENDENCY_FLAG_DISK_HANDLE</b> flag, this handle should be a handle to a 
      disk.

### -param Flags [in]

A valid combination of 
     <a href="/windows/win32/api/virtdisk/ne-virtdisk-get_storage_dependency_flag">GET_STORAGE_DEPENDENCY_FLAG</a> values.

### -param StorageDependencyInfoSize [in]

Size, in bytes, of the buffer that the <i>StorageDependencyInfo</i> parameter refers 
     to.

### -param StorageDependencyInfo [in, out]

A pointer to a buffer to receive the populated 
     [STORAGE_DEPENDENCY_INFO](./ns-virtdisk-storage_dependency_info.md) structure, which is a 
     variable-length structure.

### -param SizeUsed [in, out, optional]

An optional pointer to a <b>ULONG</b> that receives the size used.

## -returns

Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b> and the 
      <i>StorageDependencyInfo</i> parameter contains the requested dependency information.

If the function fails, the return value is an error code and the 
      <i>StorageDependencyInfo</i> parameter is undefined. For more information, see 
      <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

CD and DVD image files (ISO) are not supported before Windows 8 and 
    Windows Server 2012.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>