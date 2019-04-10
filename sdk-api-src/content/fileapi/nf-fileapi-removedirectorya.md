---
UID: NF:fileapi.RemoveDirectoryA
title: RemoveDirectoryA function (fileapi.h)
author: windows-sdk-content
description: Deletes an existing empty directory.
old-location: fs\removedirectory.htm
tech.root: FileIO
ms.assetid: d699cdd2-e270-4f17-bdec-6eea25b01578
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RemoveDirectory, RemoveDirectory function [Files], RemoveDirectoryA, RemoveDirectoryW, _win32_removedirectory, base.removedirectory, fileapi/RemoveDirectory, fileapi/RemoveDirectoryA, fileapi/RemoveDirectoryW, fs.removedirectory, winbase/RemoveDirectory, winbase/RemoveDirectoryA, winbase/RemoveDirectoryW
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RemoveDirectoryA function


## -description


Deletes an existing empty directory.

To perform this operation as a transacted operation, use the 
    <a href="https://msdn.microsoft.com/e8600166-62dc-4398-9e16-43b07f7f0b89">RemoveDirectoryTransacted</a> function.


## -parameters




### -param lpPathName [in]

The path of the directory to be removed. This path must specify an empty directory, and the calling process 
       must have delete access to the directory.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>RemoveDirectoryW</b>), you can opt-in to remove the <b>MAX_PATH</b> limitation without prepending "\\?\". See the "Maximum Path Length Limitation" section of <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>RemoveDirectory</b> function marks a directory for 
    deletion on close. Therefore, the directory is not removed until the last handle to the directory is closed.

To recursively delete the files in a directory, use the 
    <a href="https://msdn.microsoft.com/7807015f-52c5-46f5-9e90-4e3e60ddf705">SHFileOperation</a> function.

<b>RemoveDirectory</b> removes a directory junction, even 
    if the contents of the target are not empty; the function removes directory junctions regardless of the state of 
    the target object. For more information on junctions, see 
    <a href="https://msdn.microsoft.com/f9e40a86-a4a6-4524-8045-312da72dc655">Hard Links and Junctions</a>.

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
 




## -see-also




<a href="https://msdn.microsoft.com/f8ca8b10-c8bd-4285-8a40-dbec4c24729c">CreateDirectory</a>



<a href="https://msdn.microsoft.com/52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32">Creating and Deleting Directories</a>



<a href="https://msdn.microsoft.com/5517b0e7-2264-4173-8e10-ff7626458bfa">Directory Management Functions</a>



<a href="https://msdn.microsoft.com/e8600166-62dc-4398-9e16-43b07f7f0b89">RemoveDirectoryTransacted</a>
 

 

