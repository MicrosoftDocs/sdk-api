---
UID: NF:fileapifromapp.SetFileAttributesFromAppW
tech.root: fs
title: SetFileAttributesFromAppW
ms.date: 03/23/2021
targetos: Windows
description: Sets the attributes for a file or directory. The behavior of this function is identical to SetFileAttributes, except that this function adheres to the Universal Windows Platform app security model.
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
- SetFileAttributesFromAppW
- SetFileAttributesFromApp
api_type:
- DLLExport
f1_keywords:
 - SetFileAttributesFromAppW
 - fileapifromapp/SetFileAttributesFromAppW
dev_langs:
 - c++
---

## -description

Sets the attributes for a file or directory. The behavior of this function is identical to [**SetFileAttributes**](../fileapi/nf-fileapi-setfileattributesw.md), except that this function adheres to the Universal Windows Platform app security model.


## -parameters

### -param lpFileName

The name of the file whose attributes are to be set.
    
For information about opting out of the **MAX\_PATH** limitation without prepending "\\\\?\\", see the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.



### -param dwFileAttributes

The file attributes to set for the file.
    
This parameter can be one or more values, combined using the bitwise-OR operator. However, all other values override **FILE\_ATTRIBUTE\_NORMAL**.

Not all attributes are supported by this function.

The following is a list of supported attribute values.

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
<td><span id="FILE_ATTRIBUTE_ARCHIVE"></span><span id="file_attribute_archive"></span>
<strong>FILE_ATTRIBUTE_ARCHIVE</strong>
32 (0x20)</td>
<td><p>A file or directory that is an archive file or directory. Applications typically use this attribute to mark files for backup or removal.</p></td>
</tr>
<tr class="even">
<td><span id="FILE_ATTRIBUTE_HIDDEN"></span><span id="file_attribute_hidden"></span>
<strong>FILE_ATTRIBUTE_HIDDEN</strong>
2 (0x2)</td>
<td><p>The file or directory is hidden. It is not included in an ordinary directory listing.</p></td>
</tr>
<tr class="odd">
<td><span id="FILE_ATTRIBUTE_NORMAL"></span><span id="file_attribute_normal"></span>
<strong>FILE_ATTRIBUTE_NORMAL</strong>
128 (0x80)</td>
<td><p>A file that does not have other attributes set. This attribute is valid only when used alone.</p></td>
</tr>
<tr class="even">
<td><span id="FILE_ATTRIBUTE_NOT_CONTENT_INDEXED"></span><span id="file_attribute_not_content_indexed"></span>
<strong>FILE_ATTRIBUTE_NOT_CONTENT_INDEXED</strong>
8192 (0x2000)</td>
<td><p>The file or directory is not to be indexed by the content indexing service.</p></td>
</tr>
<tr class="odd">
<td><span id="FILE_ATTRIBUTE_OFFLINE"></span><span id="file_attribute_offline"></span>
<strong>FILE_ATTRIBUTE_OFFLINE</strong>
4096 (0x1000)</td>
<td><p>The data of a file is not available immediately. This attribute indicates that the file data is physically moved to offline storage. This attribute is used by Remote Storage, which is the hierarchical storage management software. Applications should not arbitrarily change this attribute.</p></td>
</tr>
<tr class="even">
<td><span id="FILE_ATTRIBUTE_READONLY"></span><span id="file_attribute_readonly"></span>
<strong>FILE_ATTRIBUTE_READONLY</strong>
1 (0x1)</td>
<td><p>A file that is read-only. Applications can read the file, but cannot write to it or delete it. This attribute is not honored on directories.</p></td>
</tr>
<tr class="odd">
<td><span id="FILE_ATTRIBUTE_SYSTEM"></span><span id="file_attribute_system"></span>
<strong>FILE_ATTRIBUTE_SYSTEM</strong>
4 (0x4)</td>
<td><p>A file or directory that the operating system uses a part of, or uses exclusively.</p></td>
</tr>
<tr class="even">
<td><span id="FILE_ATTRIBUTE_TEMPORARY"></span><span id="file_attribute_temporary"></span>
<strong>FILE_ATTRIBUTE_TEMPORARY</strong>
256 (0x100)</td>
<td><p>A file that is being used for temporary storage. File systems avoid writing data back to mass storage if sufficient cache memory is available, because typically, an application deletes a temporary file after the handle is closed. In that scenario, the system can entirely avoid writing the data. Otherwise, the data is written after the handle is closed.</p></td>
</tr>
</tbody>
</table>
    

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md).


## -remarks

## -see-also

