---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# GetCompressedFileSizeW function


## -description


Retrieves the actual number of bytes of disk storage used to store a specified file. If the file is located on a volume that supports compression and the file is compressed, the value obtained is the compressed size of the specified file. If the file is located on a volume that supports sparse files and the file is a sparse file, the value obtained is the sparse size of the specified file.

To perform this operation as a transacted operation, use the <a href="https://msdn.microsoft.com/df062eb4-70e1-4ee7-b489-624938af7834">GetCompressedFileSizeTransacted</a> function.


## -parameters




### -param lpFileName [in]

The name of the file. 




Do not specify the name of a file on a nonseeking device, such as a pipe or a communications device, as its file size has no meaning.

This parameter may include the path. In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

<div class="alert"><b>Tip</b>  Starting with Windows 10, version 1607, for the unicode version of this function (<b>GetCompressedFileSizeW</b>), you can opt-in to remove the <b>MAX_PATH</b> limitation without prepending "\\?\". See the "Maximum Path Length Limitation" section of <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details.</div>
<div> </div>

### -param lpFileSizeHigh [out, optional]

The high-order <b>DWORD</b> of the compressed file size. The function's return value is the low-order <b>DWORD</b> of the compressed file size. 




This parameter can be <b>NULL</b> if the high-order <b>DWORD</b> of the compressed file size is not needed. Files less than 4 gigabytes in size do not need the high-order <b>DWORD</b>.


## -returns



If the function succeeds, the return value is the low-order <b>DWORD</b> of the actual number of bytes of disk storage used to store the specified file, and if <i>lpFileSizeHigh</i> is non-<b>NULL</b>, the function puts the high-order <b>DWORD</b> of that actual value into the <b>DWORD</b> pointed to by that parameter. This is the compressed file size for compressed files, the actual file size for noncompressed files.

If the function fails, and <i>lpFileSizeHigh</i> is <b>NULL</b>, the return value is <b>INVALID_FILE_SIZE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If the return value is <b>INVALID_FILE_SIZE</b> and <i>lpFileSizeHigh</i> is non-<b>NULL</b>, an application must call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to determine whether the function has succeeded (value is <b>NO_ERROR</b>) or failed (value is other than <b>NO_ERROR</b>).




## -remarks



An application can determine whether a volume is compressed by calling 
<a href="https://msdn.microsoft.com/c80a38e1-319e-4f15-8c8a-9d29075e1709">GetVolumeInformation</a>, then checking the status of the <b>FS_VOL_IS_COMPRESSED</b> flag in the <b>DWORD</b> value pointed to by that function's <i>lpFileSystemFlags</i> parameter.

If the file is not located on a volume that supports compression or sparse files, or if the file is not compressed or a sparse file, the value obtained is the actual file size, the same as the value returned by a call to 
<a href="https://msdn.microsoft.com/3f5d2e4a-1e05-41c0-9b7e-0155e212f6dd">GetFileSize</a>.

Symbolic link behavior—If the path points to a symbolic link, the function returns the file size of the target.

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




<a href="https://msdn.microsoft.com/35a9fb47-5a73-479c-8fe0-5a2b07705536">File Compression and Decompression</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/df062eb4-70e1-4ee7-b489-624938af7834">GetCompressedFileSizeTransacted</a>



<a href="https://msdn.microsoft.com/3f5d2e4a-1e05-41c0-9b7e-0155e212f6dd">GetFileSize</a>



<a href="https://msdn.microsoft.com/c80a38e1-319e-4f15-8c8a-9d29075e1709">GetVolumeInformation</a>



<a href="https://msdn.microsoft.com/d6bf5df7-bc12-4dec-b116-95d9109f5eb4">Symbolic Links</a>
 

 

