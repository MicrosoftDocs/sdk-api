---
UID: NF:fileapi.GetFileAttributesExW
title: GetFileAttributesExW function
author: windows-sdk-content
description: Retrieves attributes for a specified file or directory.
old-location: fs\getfileattributesex.htm
tech.root: fileio
ms.assetid: e5d84000-17c1-4517-97a7-6bd240d73814
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetFileAttributesEx, GetFileAttributesEx function [Files], GetFileAttributesExA, GetFileAttributesExW, GetFileExInfoStandard, _win32_getfileattributesex, base.getfileattributesex, fileapi/GetFileAttributesEx, fileapi/GetFileAttributesExA, fileapi/GetFileAttributesExW, fs.getfileattributesex, winbase/GetFileAttributesEx, winbase/GetFileAttributesExA, winbase/GetFileAttributesExW
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
req.unicode-ansi: GetFileAttributesExW (Unicode) and GetFileAttributesExA (ANSI)
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
 - GetFileAttributesEx
 - GetFileAttributesExA
 - GetFileAttributesExW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetFileAttributesExW function


## -description


Retrieves attributes for a specified file or directory.

To perform this operation as a transacted operation, use the 
    <a href="https://msdn.microsoft.com/dd1435da-93e5-440a-913a-9e40e39b4a01">GetFileAttributesTransacted</a> function.


## -parameters




### -param lpFileName [in]

The name of the file or directory.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function (<b>GetFileAttributesExW</b>), and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

<div class="alert"><b>Tip</b>  Starting in Windows 10, version 1607, for the unicode version of this function (<b>GetFileAttributesExW</b>), you can opt-in to remove the <b>MAX_PATH</b> character limitation without prepending "\\?\". See the "Maximum Path Limitation" section of  <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a> for details. </div>
<div> </div>

### -param fInfoLevelId [in]

A class of attribute information to retrieve.

This parameter can be the following value from the 
      <a href="https://msdn.microsoft.com/1004ab99-9c08-4ed4-ba5f-d72f1b44a415">GET_FILEEX_INFO_LEVELS</a> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GetFileExInfoStandard"></a><a id="getfileexinfostandard"></a><a id="GETFILEEXINFOSTANDARD"></a><dl>
<dt><b>GetFileExInfoStandard</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpFileInformation</i> parameter is a 
        <a href="https://msdn.microsoft.com/e1a7fb5c-2d69-40e3-b9d8-b583a03d828a">WIN32_FILE_ATTRIBUTE_DATA</a> 
        structure.

</td>
</tr>
</table>
 


### -param lpFileInformation [out]

A pointer to a buffer that receives the attribute information.

The type of attribute information that is stored into this buffer is determined by the value of 
       <i>fInfoLevelId</i>.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero (0). To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a> function retrieves file 
    system attribute information. <b>GetFileAttributesEx</b> 
    can obtain other sets of file or directory attribute information. Currently, 
    <b>GetFileAttributesEx</b> retrieves a set of standard 
    attributes that is a superset of the file system attribute information.

When the <b>GetFileAttributesEx</b> function is 
    called on a directory that is a mounted folder, it returns the attributes of the directory, not those of the root 
    directory in the volume that the mounted folder associates with the directory. To obtain the attributes of the 
    associated volume, call 
    <a href="https://msdn.microsoft.com/3f749042-bdc9-4087-bb8a-d833713472eb">GetVolumeNameForVolumeMountPoint</a> to 
    obtain the name of the associated volume. Then use the resulting name in a call to 
    <b>GetFileAttributesEx</b>. The results are the attributes 
    of the root directory on the associated volume.

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
      the transaction is committed.  So if a transacted thread opens the file first, any subsequent threads that try 
      modifying the file before the transaction is committed receives a sharing violation.  If a non-transacted thread 
      modifies the file before the transacted thread does, and the file is still open when the transaction attempts to 
      open it, the transaction receives the error <b>ERROR_TRANSACTIONAL_CONFLICT</b>.




## -see-also




<a href="https://msdn.microsoft.com/ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156">File Attribute Constants</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a>



<a href="https://msdn.microsoft.com/dd1435da-93e5-440a-913a-9e40e39b4a01">GetFileAttributesTransacted</a>



<a href="https://msdn.microsoft.com/3d5400c3-555f-44fc-9470-52a36d04d90b">SetFileAttributes</a>



<a href="https://msdn.microsoft.com/d6bf5df7-bc12-4dec-b116-95d9109f5eb4">Symbolic Links</a>
 

 

