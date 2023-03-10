---
UID: NF:fileapi.GetDiskSpaceInformationW
tech.root: fs
title: GetDiskSpaceInformationW function (fileapi.h)
ms.date: 01/05/2023
targetos: Windows
description: Gets disk space information for a volume at a given root path.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: fileapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - 
api_location:
 - fileapi.h
api_name:
 - GetDiskSpaceInformationW
 - GetDiskSpaceInformation
f1_keywords:
 - GetDiskSpaceInformationW
 - fileapi/GetDiskSpaceInformationW
 - GetDiskSpaceInformation
 - fileapi/GetDiskSpaceInformation
dev_langs:
 - c++
helpviewer_keywords:
 - GetDiskSpaceInformationW
---

## -description

Gets disk space information for a volume at a given root path.

## -parameters

### -param rootPath

A pointer to a string that contains the root directory of the volume to be queried.

If this parameter is `NULL`, the function uses the root of the current disk.

### -param diskSpaceInfo

A [**DISK_SPACE_INFORMATION**](ns-fileapi-disk_space_information.md) structure containing information about the current disk space for the volume at the given root path.

## -returns

Returns `TRUE` if the function succeeds, or `FALSE` if it fails. To get extended error information, call the `GetLastError` function.

## -remarks

The `rootPath` must be a root path, such as `C:\` or `D:\`, and not a subdirectory of a root path.

## -see-also

[GetDiskSpaceInformationA](nf-fileapi-getdiskspaceinformationa.md)

[DISK_SPACE_INFORMATION](ns-fileapi-disk_space_information.md)
