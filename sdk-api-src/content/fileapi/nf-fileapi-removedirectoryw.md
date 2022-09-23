---
UID: NF:fileapi.RemoveDirectoryW
title: RemoveDirectoryW function (fileapi.h)
description: Deletes an existing empty directory. (Unicode)
helpviewer_keywords: ["RemoveDirectory","RemoveDirectory function [Files]","RemoveDirectoryA","RemoveDirectoryW","_win32_removedirectory","base.removedirectory","fileapi/RemoveDirectory","fileapi/RemoveDirectoryA","fileapi/RemoveDirectoryW","fs.removedirectory","winbase/RemoveDirectory","winbase/RemoveDirectoryA","winbase/RemoveDirectoryW"]
old-location: fs\removedirectory.htm
tech.root: fs
ms.assetid: d699cdd2-e270-4f17-bdec-6eea25b01578
ms.date: 12/05/2018
ms.keywords: RemoveDirectory, RemoveDirectory function [Files], RemoveDirectoryA, RemoveDirectoryW, _win32_removedirectory, base.removedirectory, fileapi/RemoveDirectory, fileapi/RemoveDirectoryA, fileapi/RemoveDirectoryW, fs.removedirectory, winbase/RemoveDirectory, winbase/RemoveDirectoryA, winbase/RemoveDirectoryW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RemoveDirectoryW (Unicode) and RemoveDirectoryA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RemoveDirectoryW
 - fileapi/RemoveDirectoryW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - RemoveDirectory
 - RemoveDirectoryA
 - RemoveDirectoryW
---

# RemoveDirectoryW function


## -description

Deletes an existing empty directory.

To perform this operation as a transacted operation, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-removedirectorytransacteda">RemoveDirectoryTransacted</a> function.

## -parameters

### -param lpPathName [in]

The path of the directory to be removed. This path must specify an empty directory, and the calling process 
       must have delete access to the directory.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\\\?\\" to the path. For more information, see 
       <a href="/windows/desktop/FileIO/naming-a-file">Naming a File</a>.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>RemoveDirectoryW</b>), you can opt-in to remove the <b>MAX_PATH</b> limitation without prepending "\\?\". See the "Maximum Path Length Limitation" section of <a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>RemoveDirectory</b> function marks a directory for 
    deletion on close. Therefore, the directory is not removed until the last handle to the directory is closed.

To recursively delete the files in a directory, use the 
    <a href="/windows/desktop/api/shellapi/nf-shellapi-shfileoperationa">SHFileOperation</a> function.

<b>RemoveDirectory</b> removes a directory junction, even 
    if the contents of the target are not empty; the function removes directory junctions regardless of the state of 
    the target object. For more information on junctions, see 
    <a href="/windows/desktop/FileIO/hard-links-and-junctions">Hard Links and Junctions</a>.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

<table>
<tr>
<th>Technology</th>
<th>Supported</th>
</tr>
<tr>
<td>
Server Message Block (SMB) 3.0 protocol

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
Yes

</td>
</tr>
</table>
 





> [!NOTE]
> The fileapi.h header defines RemoveDirectory as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createdirectorya">CreateDirectory</a>



<a href="/windows/desktop/FileIO/creating-and-deleting-directories">Creating and Deleting Directories</a>



<a href="/windows/desktop/FileIO/directory-management-functions">Directory Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-removedirectorytransacteda">RemoveDirectoryTransacted</a>
