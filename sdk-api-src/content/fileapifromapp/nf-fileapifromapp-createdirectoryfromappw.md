---
UID: NF:fileapifromapp.CreateDirectoryFromAppW
tech.root: fs
title: CreateDirectoryFromAppW
ms.date: 03/23/2021
targetos: Windows
description: Creates a new directory. The behavior of this function is identical to CreateDirector, except that this function adheres to the Universal Windows Platform app security model.
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
 - api-ms-win-core-file-fromapp-l1-1-0.dll
api_name:
- CreateDirectoryFromAppW
- CreateDirectoryFromApp
api_type:
- DLLExport
f1_keywords:
 - CreateDirectoryFromAppW
 - fileapifromapp/CreateDirectoryFromAppW
helpviewer_keywords:
 - CreateDirectoryFromAppW
 - fileapifromapp/CreateDirectoryFromAppW
dev_langs:
 - c++
---

## -description

Creates a new directory. The behavior of this function is identical to [**CreateDirectory**](../winbase/nf-winbase-createdirectory.md), except that this function adheres to the Universal Windows Platform app security model.


## -parameters

### -param lpPathName

The path of the directory to be created.
     
For information about opting out of the **MAX\_PATH** limitation without prepending "\\\\?\\", see the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.


### -param lpSecurityAttributes

A pointer to a [**SECURITY\_ATTRIBUTES**](../wtypesbase/ns-wtypesbase-security_attributes.md) structure. The **lpSecurityDescriptor** member of the structure specifies a security descriptor for the new directory. If *lpSecurityAttributes* is **NULL**, the directory gets a default security descriptor. The ACLs in the default security descriptor for a directory are inherited from its parent directory.
    
The target file system must support security on files and directories for this parameter to have an effect.


## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md). Possible errors include the following.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th>Return code</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ERROR_ALREADY_EXISTS</strong></td>
<td><p>The specified directory already exists.</p></td>
</tr>
<tr class="even">
<td><strong>ERROR_PATH_NOT_FOUND</strong></td>
<td><p>One or more intermediate directories do not exist; this function will only create the final directory in the path.</p></td>
</tr>
</tbody>
</table>


## -remarks

## -see-also

