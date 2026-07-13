---
UID: NF:fileapifromapp.RemoveDirectoryFromAppW
tech.root: fs
title: RemoveDirectoryFromAppW
ms.date: 03/21/2023
targetos: Windows
description: Deletes an existing empty directory. The behavior of this function is identical to RemoveDirectory, except that this function adheres to the Universal Windows Platform app security model.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: fileapifromapp.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: OneCore.Lib
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
- RemoveDirectoryFromAppW
- RemoveDirectoryFromApp
api_type:
- DLLExport
f1_keywords:
 - RemoveDirectoryFromAppW
 - fileapifromapp/RemoveDirectoryFromAppW
dev_langs:
 - c++
---

## -description

Deletes an existing empty directory. The behavior of this function is identical to [RemoveDirectory](../fileapi/nf-fileapi-removedirectoryw.md), except that this function adheres to the Universal Windows Platform (UWP) app security model.

## -parameters

### -param lpPathName

The path of the directory to be removed. This path must specify an empty directory, and the calling process must have delete access to the directory.

For information about opting out of the **MAX\_PATH** limitation without prepending "\\\\?\\", see the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (`0`). To get extended error information, call [GetLastError](../errhandlingapi/nf-errhandlingapi-getlasterror.md).

## -remarks

## -see-also

[Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file)

[RemoveDirectory](../fileapi/nf-fileapi-removedirectoryw.md)
