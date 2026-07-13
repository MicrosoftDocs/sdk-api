---
UID: NF:fileapifromapp.DeleteFileFromAppW
tech.root: fs
title: DeleteFileFromAppW
ms.date: 03/23/2021
targetos: Windows
description: Deletes an existing file. The behavior of this function is identical to DeleteFile, except that this function adheres to the Universal Windows Platform app security model.
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
- sqlite.dll
- api-ms-win-core-file-fromapp-l1-1-0.dll
api_name:
- DeleteFileFromAppW
- DeleteFileFromApp
api_type:
- DLLExport
f1_keywords:
 - DeleteFileFromAppW
 - fileapifromapp/DeleteFileFromAppW
dev_langs:
 - c++
---

## -description

Deletes an existing file. The behavior of this function is identical to [**DeleteFile**](../fileapi/nf-fileapi-deletefilew.md), except that this function adheres to the Universal Windows Platform app security model.


## -parameters

### -param lpFileName

The name of the file to be deleted.
    
In the ANSI version of this function, the name is limited to **MAX\_PATH** characters. To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

For the unicode version of this function (**DeleteFileFromAppW**), you can opt-in to remove the **MAX\_PATH** character limitation without prepending "\\\\?\\". See the "Maximum Path Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.


## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md).


## -remarks

## -see-also

