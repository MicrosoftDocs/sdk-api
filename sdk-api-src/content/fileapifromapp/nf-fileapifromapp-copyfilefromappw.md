---
UID: NF:fileapifromapp.CopyFileFromAppW
tech.root: fs
title: CopyFileFromAppW
ms.date: 03/23/2021
targetos: Windows
description: Copies an existing file to a new file. The behavior of this function is identical to CopyFile, except that this function adheres to the Universal Windows Platform app security model.
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
- CopyFileFromAppW
- CopyFileFromApp
api_type:
- DLLExport
f1_keywords:
 - CopyFileFromAppW
 - fileapifromapp/CopyFileFromAppW
dev_langs:
 - c++
---

## -description

Copies an existing file to a new file. The behavior of this function is identical to [**CopyFile**](../winbase/nf-winbase-copyfile.md), except that this function adheres to the Universal Windows Platform app security model.


## -parameters

### -param lpExistingFileName

The name of an existing file.
    
For information about opting out of the **MAX\_PATH** limitation without prepending "\\\\?\\", see the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

If *lpExistingFileName* does not exist, the function fails, and [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md) returns **ERROR\_FILE\_NOT\_FOUND**.


### -param lpNewFileName

The name of the new file.

In the ANSI version of this function, the name is limited to **MAX\_PATH** characters. To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend "\\\\?\\" to the path. For more information, see [Naming a File](/windows/win32/FileIO/naming-a-file).

For the unicode version of this function (**CopyFileFromAppW**), you can opt-in to remove the **MAX\_PATH** limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/FileIO/naming-a-file) for details.


### -param bFailIfExists

If this parameter is **TRUE** and the new file specified by *lpNewFileName* already exists, the function fails. If this parameter is **FALSE** and the new file already exists, the function overwrites the existing file and succeeds.


## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md).


## -remarks

## -see-also

