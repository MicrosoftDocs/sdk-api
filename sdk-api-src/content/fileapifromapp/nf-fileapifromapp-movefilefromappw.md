---
UID: NF:fileapifromapp.MoveFileFromAppW
tech.root: fs
title: MoveFileFromAppW
ms.date: 03/23/2021
targetos: Windows
description: Moves an existing file or a directory, including its children. The behavior of this function is identical to MoveFile, except that this function adheres to the Universal Windows Platform app security model.
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
 - api-ms-win-core-file-fromapp-l1-1-0.dll
api_name:
- MoveFileFromAppW
- MoveFileFromApp
api_type:
- DLLExport
f1_keywords:
 - MoveFileFromAppW
 - fileapifromapp/MoveFileFromAppW
dev_langs:
 - c++
---

## -description

Moves an existing file or a directory, including its children. The behavior of this function is identical to [**MoveFile**](../winbase/nf-winbase-movefile.md), except that this function adheres to the Universal Windows Platform app security model.


## -parameters

### -param lpExistingFileName

The current name of the file or directory on the local computer.
    
For information about opting out of the **MAX\_PATH** limitation without prepending "\\\\?\\", see the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.




### -param lpNewFileName

The new name for the file or directory. The new name must not already exist. A new file may be on a different file system or drive. A new directory must be on the same drive.
    
For information about opting out of the **MAX\_PATH** limitation without prepending "\\\\?\\", see the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.




## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md).


## -remarks

## -see-also

