---
UID: NF:fileapifromapp.GetFileAttributesExFromAppW
tech.root: fs
title: GetFileAttributesExFromAppW
ms.date: 03/21/2023
targetos: Windows
description: Retrieves attributes for a specified file or directory. The behavior of this function is identical to GetFileAttributesEx, except that this function adheres to the Universal Windows Platform app security model.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: fileapifromapp.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 1803
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_location:
 - Kernel32.dll
api_name:
- GetFileAttributesFromAppW
- GetFileAttributesFromApp
api_type:
- DLLExport
f1_keywords:
 - GetFileAttributesExFromAppW
 - fileapifromapp/GetFileAttributesExFromAppW
dev_langs:
 - c++
---

## -description

Retrieves attributes for a specified file or directory. The behavior of this function is identical to [GetFileAttributesEx](../fileapi/nf-fileapi-getfileattributesexw.md), except that this function adheres to the Universal Windows Platform (UWP) app security model.

## -parameters

### -param lpFileName

The name of the file or directory.

For information about opting out of the **MAX\_PATH** limitation without prepending "\\\\?\\", see the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param fInfoLevelId

A class of attribute information to retrieve.

This parameter can be the following value from the [GET\_FILEEX\_INFO\_LEVELS](../minwinbase/ne-minwinbase-get_fileex_info_levels.md) enumeration.

| Value | Meaning |
|--------|--------|
| **GetFileExInfoStandard** | The _lpFileInformation_ parameter is a [WIN32_FILE_ATTRIBUTE_DATA](/windows/win32/api/fileapi/ns-fileapi-win32_file_attribute_data) structure. |

### -param lpFileInformation

A pointer to a buffer that receives the attribute information.

The type of attribute information that is stored into this buffer is determined by the value of _fInfoLevelId_.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero (`0`). To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -remarks

## -see-also

[Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file)

[GetFileAttributesEx](../fileapi/nf-fileapi-getfileattributesexw.md)
