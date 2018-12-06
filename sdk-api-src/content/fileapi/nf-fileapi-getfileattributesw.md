---
UID: NF:fileapi.GetFileAttributesW
title: GetFileAttributesW function
author: windows-sdk-content
description: Retrieves file system attributes for a specified file or directory.
old-location: fs\getfileattributes.htm
tech.root: fileio
ms.assetid: 9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFileAttributes, GetFileAttributes function [Files], GetFileAttributesA, GetFileAttributesW, _win32_getfileattributes, base.getfileattributes, fileapi/GetFileAttributes, fileapi/GetFileAttributesA, fileapi/GetFileAttributesW, fs.getfileattributes, winbase/GetFileAttributes, winbase/GetFileAttributesA, winbase/GetFileAttributesW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetFileAttributesW (Unicode) and GetFileAttributesA (ANSI)
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
 - GetFileAttributes
 - GetFileAttributesA
 - GetFileAttributesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetFileAttributesW function


## -description


Retrieves file system attributes for a specified file or directory.

To get more attribute information, use the 
    <a href="https://msdn.microsoft.com/e5d84000-17c1-4517-97a7-6bd240d73814">GetFileAttributesEx</a> function.

To perform this operation as a transacted operation, use the 
    <a href="https://msdn.microsoft.com/dd1435da-93e5-440a-913a-9e40e39b4a01">GetFileAttributesTransacted</a> function.


## -parameters




### -param lpFileName [in]

The name of the file or directory. 
      

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function (<b>GetFileAttributesW</b>), and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">File Names, Paths, and Namespaces</a>.

<div class="alert"><b>Tip</b>  Starting in Windows 10, version 1607, for the unicode version of this function (<b>GetFileAttributesW</b>), you can opt-in to remove the <b>MAX_PATH</b> character limitation without prepending "\\?\". See the "Maximum Path Limitation" section of  <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details. </div>
<div> </div>

## -returns



If the function succeeds, the return value contains the attributes of the specified file or directory. For a 
       list of attribute values and their descriptions, see 
       <a href="https://msdn.microsoft.com/ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156">File Attribute Constants</a>.

If the function fails, the return value is <b>INVALID_FILE_ATTRIBUTES</b>. To get extended 
       error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When <b>GetFileAttributes</b> is called on a directory 
    that is a mounted folder, it returns the file system attributes of the directory, not those of the root directory 
    in the volume that the mounted folder associates with the directory. To obtain the file attributes of the 
    associated volume, call 
    <a href="https://msdn.microsoft.com/3f749042-bdc9-4087-bb8a-d833713472eb">GetVolumeNameForVolumeMountPoint</a> to 
    obtain the name of the associated volume. Then use the resulting name in a call to 
    <b>GetFileAttributes</b>. The results are the attributes of 
    the root directory on the associated volume.

If you call <b>GetFileAttributes</b> for a network share, 
    the function fails, and <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
    <b>ERROR_BAD_NETPATH</b>. You must specify a path to a subfolder on that share.

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
 

Symbolic link behavior—If the path points to a symbolic link, the function returns 
    attributes for the symbolic link.

<h3><a id="Transacted_Operations"></a><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
If a file is open for modification in a transaction, no other thread can open the file for modification until 
      the transaction is committed. So if a transacted thread opens the file first, any subsequent threads that try 
      modifying the file before the transaction is committed receives a sharing violation. If a non-transacted thread 
      modifies the file before the transacted thread does, and the file is still open when the transaction attempts to 
      open it, the transaction receives the error <b>ERROR_TRANSACTIONAL_CONFLICT</b>.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/f6eaea8a-0cc2-4fb6-bec5-7fb12b20c075">Retrieving and Changing File Attributes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156">File Attribute Constants</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/02fc92c4-582d-4c9f-a811-b5c839e9fffa">FindFirstFile</a>



<a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a>



<a href="https://msdn.microsoft.com/e5d84000-17c1-4517-97a7-6bd240d73814">GetFileAttributesEx</a>



<a href="https://msdn.microsoft.com/dd1435da-93e5-440a-913a-9e40e39b4a01">GetFileAttributesTransacted</a>



<a href="https://msdn.microsoft.com/3d5400c3-555f-44fc-9470-52a36d04d90b">SetFileAttributes</a>



<a href="https://msdn.microsoft.com/d6bf5df7-bc12-4dec-b116-95d9109f5eb4">Symbolic Links</a>
 

 

