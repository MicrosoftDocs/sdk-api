---
UID: NF:fileapifromapp.FindFirstFileExFromAppW
tech.root: fs
title: FindFirstFileExFromAppW
ms.date: 03/23/2021
targetos: Windows
description: Searches a directory for a file or subdirectory with a name and attributes that match those specified.
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
- GetFileAttributesFromAppW
- GetFileAttributesFromApp
api_type:
- DLLExport
f1_keywords:
 - FindFirstFileExFromAppW
 - fileapifromapp/FindFirstFileExFromAppW
dev_langs:
 - c++
---

## -description

Searches a directory for a file or subdirectory with a name and attributes that match those specified. The behavior of this function is identical to [**FindFirstFileEx**](../fileapi/nf-fileapi-findfirstfileexw.md), except that this function adheres to the Universal Windows Platform app security model.


## -parameters

### -param lpFileName

The directory or path, and the file name. The file name can include wildcard characters, for example, an asterisk (\*) or a question mark (?).
    
This parameter should not be **NULL**, an invalid string (for example, an empty string or a string that is missing the terminating null character), or end in a trailing backslash (\\).

If the string ends with a wildcard, period, or directory name, the user must have access to the root and all subdirectories on the path.

For information about opting out of the **MAX\_PATH** limitation without prepending "\\\\?\\", see the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.


### -param fInfoLevelId

The information level of the returned data.
    
This parameter is one of the [**FINDEX\_INFO\_LEVELS**](../minwinbase/ne-minwinbase-findex_info_levels.md) enumeration values.


### -param lpFindFileData

A pointer to the buffer that receives the file data.
    
The pointer type is determined by the level of information that is specified in the *fInfoLevelId* parameter.


### -param fSearchOp

The type of filtering to perform that is different from wildcard matching.
    
This parameter is one of the [**FINDEX\_SEARCH\_OPS**](../minwinbase/ne-minwinbase-findex_search_ops.md) enumeration values.


### -param lpSearchFilter

A pointer to the search criteria if the specified *fSearchOp* needs structured search information.

At this time, none of the supported *fSearchOp* values require extended search information. Therefore, this pointer must be **NULL**.


### -param dwAdditionalFlags

Specifies additional flags that control the search.
    
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
<td><span id="FIND_FIRST_EX_CASE_SENSITIVE"></span><span id="find_first_ex_case_sensitive"></span>
<strong>FIND_FIRST_EX_CASE_SENSITIVE</strong>
1</td>
<td><p>Searches are case-sensitive.</p></td>
</tr>
<tr class="even">
<td><span id="FIND_FIRST_EX_LARGE_FETCH"></span><span id="find_first_ex_large_fetch"></span>
<strong>FIND_FIRST_EX_LARGE_FETCH</strong>
2</td>
<td><p>Uses a larger buffer for directory queries, which can increase performance of the find operation.</p></td>
</tr>
<tr class="odd">
<td><span id="FIND_FIRST_EX_ON_DISK_ENTRIES_ONLY"></span><span id="find_first_ex_on_disk_entries_only"></span>
<strong>FIND_FIRST_EX_ON_DISK_ENTRIES_ONLY</strong>
4</td>
<td><p>Limits the results to files that are physically on disk. This flag is only relevant when a file virtualization filter is present.</p></td>
</tr>
</tbody>
</table>

## -returns

If the function succeeds, the return value is a search handle used in a subsequent call to [**FindNextFile**](../fileapi/nf-fileapi-findnextfilew.md) or [**FindClose**](../fileapi/nf-fileapi-findclose.md), and the *lpFindFileData* parameter contains information about the first file or directory found.

If the function fails or fails to locate files from the search string in the *lpFileName* parameter, the return value is **INVALID\_HANDLE\_VALUE** and the contents of *lpFindFileData* are indeterminate. To get extended error information, call the [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md) function.


## -remarks

## -see-also

