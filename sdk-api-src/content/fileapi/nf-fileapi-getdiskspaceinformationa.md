---
UID: NF:fileapi.GetDiskSpaceInformationA
tech.root: fs
title: GetDiskSpaceInformationA function (fileapi.h)
ms.date: 01/05/2023
targetos: Windows
description: Gets disk space information for a volume at a given root path.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: kernel32.dll
req.header: fileapi.h
req.idl: 
req.include-header: Windows.h
req.irql: 
req.kmdf-ver: 
req.lib: kernel32.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 17763 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 10 Server 2019 [desktop apps \| UWP apps]
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-File-l1-2-3
api_name:
 - GetDiskSpaceInformationA
 - GetDiskSpaceInformation
f1_keywords:
 - GetDiskSpaceInformationA
 - fileapi/GetDiskSpaceInformationA
 - GetDiskSpaceInformation
 - fileapi/GetDiskSpaceInformation
dev_langs:
 - c++
helpviewer_keywords:
 - GetDiskSpaceInformationA
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

[GetDiskSpaceInformationW](nf-fileapi-getdiskspaceinformationw.md)

[DISK_SPACE_INFORMATION](ns-fileapi-disk_space_information.md)
