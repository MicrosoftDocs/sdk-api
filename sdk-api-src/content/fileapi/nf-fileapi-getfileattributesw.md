---
UID: NF:fileapi.GetFileAttributesW
title: GetFileAttributesW function (fileapi.h)
description: Retrieves file system attributes for a specified file or directory.helpviewer_keywords: ["GetFileAttributes","GetFileAttributes function [Files]","GetFileAttributesA","GetFileAttributesW","_win32_getfileattributes","base.getfileattributes","fileapi/GetFileAttributes","fileapi/GetFileAttributesA","fileapi/GetFileAttributesW","fs.getfileattributes","winbase/GetFileAttributes","winbase/GetFileAttributesA","winbase/GetFileAttributesW"]
old-location: fs\getfileattributes.htm
tech.root: FileIO
ms.assetid: 9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690
ms.date: 12/05/2018
ms.keywords: GetFileAttributes, GetFileAttributes function [Files], GetFileAttributesA, GetFileAttributesW, _win32_getfileattributes, base.getfileattributes, fileapi/GetFileAttributes, fileapi/GetFileAttributesA, fileapi/GetFileAttributesW, fs.getfileattributes, winbase/GetFileAttributes, winbase/GetFileAttributesA, winbase/GetFileAttributesW
f1_keywords:
- fileapi/GetFileAttributes
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetFileAttributesW function


## -description


Retrieves file system attributes for a specified file or directory.

To get more attribute information, use the 
    <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getfileattributesexa">GetFileAttributesEx</a> function.

To perform this operation as a transacted operation, use the 
    <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getfileattributestransacteda">GetFileAttributesTransacted</a> function.


## -parameters




### -param lpFileName [in]

The name of the file or directory. 
      

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function (<b>GetFileAttributesW</b>), and prepend 
       "\\\\?\\" to the path. For more information, see 
       <a href="https://docs.microsoft.com/windows/desktop/FileIO/naming-a-file">File Names, Paths, and Namespaces</a>.

<div class="alert"><b>Tip</b>  Starting in Windows 10, version 1607, for the unicode version of this function (<b>GetFileAttributesW</b>), you can opt-in to remove the <b>MAX_PATH</b> character limitation without prepending "\\?\". See the "Maximum Path Limitation" section of  <a href="https://docs.microsoft.com/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a> for details. </div>
<div> </div>

## -returns



If the function succeeds, the return value contains the attributes of the specified file or directory. For a 
       list of attribute values and their descriptions, see 
       <a href="https://docs.microsoft.com/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>.

If the function fails, the return value is <b>INVALID_FILE_ATTRIBUTES</b>. To get extended 
       error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



When <b>GetFileAttributes</b> is called on a directory 
    that is a mounted folder, it returns the file system attributes of the directory, not those of the root directory 
    in the volume that the mounted folder associates with the directory. To obtain the file attributes of the 
    associated volume, call 
    <a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getvolumenameforvolumemountpointw">GetVolumeNameForVolumeMountPoint</a> to 
    obtain the name of the associated volume. Then use the resulting name in a call to 
    <b>GetFileAttributes</b>. The results are the attributes of 
    the root directory on the associated volume.

If you call <b>GetFileAttributes</b> for a network share, 
    the function fails, and <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
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
     <a href="https://docs.microsoft.com/windows/desktop/FileIO/retrieving-and-changing-file-attributes">Retrieving and Changing File Attributes</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-findnextfilea">FindNextFile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-getfileattributesexa">GetFileAttributesEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-getfileattributestransacteda">GetFileAttributesTransacted</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-setfileattributesa">SetFileAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>
 

 

