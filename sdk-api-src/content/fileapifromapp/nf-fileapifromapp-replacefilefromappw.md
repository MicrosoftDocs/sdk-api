---
UID: NF:fileapifromapp.ReplaceFileFromAppW
tech.root: fs
title: ReplaceFileFromAppW
ms.date: 03/23/2021
targetos: Windows
description: Replaces one file with another file, with the option of creating a backup copy of the original file. The behavior of this function is identical to ReplaceFile, except that this function adheres to the Universal Windows Platform app security model.
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
- ReplaceFileFromAppW
- ReplaceFileFromApp
api_type:
- DLLExport
f1_keywords:
 - ReplaceFileFromAppW
 - fileapifromapp/ReplaceFileFromAppW
dev_langs:
 - c++
---

## -description

Replaces one file with another file, with the option of creating a backup copy of the original file. The behavior of this function is identical to [**ReplaceFile**](../winbase/nf-winbase-replacefilew.md), except that this function adheres to the Universal Windows Platform app security model.


## -parameters

### -param lpReplacedFileName

For information about opting out of the **MAX\_PATH** limitation without prepending "\\\\?\\", see the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.
    
This file is opened with the **GENERIC\_READ**, **DELETE**, and **SYNCHRONIZE** access rights. The sharing mode is **FILE\_SHARE\_READ** | **FILE\_SHARE\_WRITE** | **FILE\_SHARE\_DELETE**.
    
The caller must have write access to the file to be replaced. For more information, see [File Security and Access Rights](/windows/win32/fileio/file-security-and-access-rights).


### -param lpReplacementFileName

 The name of the file that will replace the *lpReplacedFileName* file.
    
For information about opting out of the **MAX\_PATH** limitation without prepending "\\\\?\\", see the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

    
The function attempts to open this file with the **SYNCHRONIZE**, **GENERIC\_READ**, **GENERIC\_WRITE**, **DELETE**, and **WRITE\_DAC** access rights so that it can preserve all attributes and ACLs. If this fails, the function attempts to open the file with the **SYNCHRONIZE**, **GENERIC\_READ**, **DELETE**, and **WRITE\_DAC** access rights. No sharing mode is specified.


### -param lpBackupFileName

 The name of the file that will serve as a backup copy of the *lpReplacedFileName* file. If this parameter is **NULL**, no backup file is created. See the Remarks section for implementation details on the backup file.
    
For information about opting out of the **MAX\_PATH** limitation without prepending "\\\\?\\", see the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.




### -param dwReplaceFlags

The replacement options. This parameter can be one or more of the following values.
    
<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="REPLACEFILE_WRITE_THROUGH"></span><span id="replacefile_write_through"></span>
<strong>REPLACEFILE_WRITE_THROUGH</strong>
0x00000001</td>
<td><p>This value is not supported.</p></td>
</tr>
<tr class="even">
<td><span id="REPLACEFILE_IGNORE_MERGE_ERRORS"></span><span id="replacefile_ignore_merge_errors"></span>
<strong>REPLACEFILE_IGNORE_MERGE_ERRORS</strong>
0x00000002</td>
<td><p>Ignores errors that occur while merging information (such as attributes and ACLs) from the replaced file to the replacement file. Therefore, if you specify this flag and do not have <strong>WRITE_DAC</strong> access, the function succeeds but the ACLs are not preserved.</p></td>
</tr>
<tr class="odd">
<td><span id="REPLACEFILE_IGNORE_ACL_ERRORS"></span><span id="replacefile_ignore_acl_errors"></span>
<strong>REPLACEFILE_IGNORE_ACL_ERRORS</strong>
0x00000004</td>
<td><p>Ignores errors that occur while merging ACL information from the replaced file to the replacement file. Therefore, if you specify this flag and do not have <strong>WRITE_DAC</strong> access, the function succeeds but the ACLs are not preserved. To compile an application that uses this value, define the <strong>_WIN32_WINNT</strong> macro as 0x0600 or later.</p></td>
</tr>
</tbody>
</table>
    
     

### -param lpExclude

Reserved for future use.

### -param lpReserved

Reserved for future use.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md). The following are possible error codes for this function.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th>Return code/value</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ERROR_UNABLE_TO_MOVE_REPLACEMENT</strong>
1176 (0x498)</td>
<td><p>The replacement file could not be renamed. If <em>lpBackupFileName</em> was specified, the replaced and replacement files retain their original file names. Otherwise, the replaced file no longer exists and the replacement file exists under its original name.</p></td>
</tr>
<tr class="even">
<td><strong>ERROR_UNABLE_TO_MOVE_REPLACEMENT_2</strong>
1177 (0x499)</td>
<td><p>The replacement file could not be moved. The replacement file still exists under its original name; however, it has inherited the file streams and attributes from the file it is replacing. The file to be replaced still exists with a different name. If <em>lpBackupFileName</em> is specified, it will be the name of the replaced file.</p></td>
</tr>
<tr class="odd">
<td><strong>ERROR_UNABLE_TO_REMOVE_REPLACED</strong>
1175 (0x497)</td>
<td><p>The replaced file could not be deleted. The replaced and replacement files retain their original file names.</p></td>
</tr>
</tbody>
</table>

 

If any other error is returned, such as **ERROR\_INVALID\_PARAMETER**, the replaced and replacement files will retain their original file names. In this scenario, a backup file does not exist and it is not guaranteed that the replacement file will have inherited all of the attributes and streams of the replaced file.


## -remarks

## -see-also

