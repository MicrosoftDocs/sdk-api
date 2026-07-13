---
UID: NF:fileapi.SetFileValidData
title: SetFileValidData function (fileapi.h)
description: Sets the valid data length of the specified file. This function is useful in very limited scenarios. For more information, see the Remarks section.
helpviewer_keywords: ["SetFileValidData","SetFileValidData function [Files]","_win32_setfilevaliddata","base.setfilevaliddata","fileapi/SetFileValidData","fs.setfilevaliddata","winbase/SetFileValidData"]
old-location: fs\setfilevaliddata.htm
tech.root: fs
ms.assetid: c6ded2d7-270a-4b75-b2d4-1007a92fe831
ms.date: 12/05/2018
ms.keywords: SetFileValidData, SetFileValidData function [Files], _win32_setfilevaliddata, base.setfilevaliddata, fileapi/SetFileValidData, fs.setfilevaliddata, winbase/SetFileValidData
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - SetFileValidData
 - fileapi/SetFileValidData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l1-2-5.dll
 - api-ms-win-core-file-l1-2-4.dll
 - api-ms-win-core-file-l1-2-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-0.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - SetFileValidData
---

# SetFileValidData function


## -description

Sets the valid data length of the specified file. This function is useful in very limited scenarios. For more information, see the Remarks section.<div class="alert"><b>Caution</b>  Use of this function without proper security considerations may compromise data privacy and security. For more information, see the Remarks section.</div>
<div> </div>

## -parameters

### -param hFile [in]

A handle to the file. The file must have been opened with the <b>GENERIC_WRITE</b> access right, and the <b>SE_MANAGE_VOLUME_NAME</b> privilege enabled. For more information, see 
<a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

<div class="alert"><b>Note</b>  The file cannot be a network file, or be compressed, sparse, or transacted.</div>
<div> </div>

### -param ValidDataLength [in]

The new valid data length. 

This parameter must be a positive value that is greater than the current valid data length, but less than the current file size.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>SetFileValidData</b> function sets the logical end of a file. To set the size of a file, use the <a href="/windows/desktop/api/fileapi/nf-fileapi-setendoffile">SetEndOfFile</a> function. The physical file size is also referred to as the end of the file.

Each file stream has the following properties:

<ul>
<li>File size: the size of the data in a file, to the byte.</li>
<li>Allocation size: the size of the space that is allocated for a file on a disk, which is always an even multiple of the cluster size.</li>
<li>Valid data length: the length of the data in a file that is actually written, to the byte. This value is always less than or equal to the file size.</li>
</ul>
Typically, the 
<b>SetFileValidData</b> function is used by system-level applications on their own private data.   Not all file systems  use valid data length.  Some file systems can track multiple valid data ranges.
In general, most applications will never need to call this function.

The <b>SetFileValidData</b> function allows you to avoid filling data with zeros when writing nonsequentially to a file. The function makes the data in the file valid without writing to the file. As a result, although some performance gain may be realized, existing data on disk from previously existing files can inadvertently become available to unintended readers. The following paragraphs provide a more detailed description of this potential security and privacy issue.

A caller must have the <b>SE_MANAGE_VOLUME_NAME</b> privilege enabled when opening a file initially. Applications should call <b>SetFileValidData</b> only on files that restrict access to those entities that  have <b>SE_MANAGE_VOLUME_NAME</b> access. The application must ensure that the unwritten ranges of the file are never exposed, or security issues can result as follows.

If <b>SetFileValidData</b> is used on a file, the potential performance gain is obtained by not filling the allocated clusters for the file with zeros. Therefore, reading from the file will return whatever the allocated clusters contain, potentially content from other users.  This is not necessarily a security issue at this point, because the caller needs to have <b>SE_MANAGE_VOLUME_NAME</b> privilege for <b>SetFileValidData</b> to succeed,  and all  data on disk can be read by such users.  However, this caller can inadvertently expose this data to other users that cannot acquire the <b>SE_MANAGE_VOLUME_PRIVILEGE</b> privilege if the following holds: <ul>
<li>If the file was not opened with a sharing mode that denies other readers,  a nonprivileged user can open it and read the exposed data.</li>
<li>If the system stops responding before the caller finishes writing up the <i>ValidDataLength</i> supplied in the call, then, on a reboot, such a nonprivileged user can open the file and read exposed content.</li>
</ul>


If the caller of <b>SetFileValidData</b> opened the file with adequately restrictive access control, the previous conditions would not apply. However, for partially written files extended with <b>SetFileValidData</b> (that is, writing was not completed up to the <i>ValidDataLength</i> supplied in the call) there exists yet another potential privacy or security vulnerability. An administrator could copy the file to a target that is not properly controlled with restrictive ACL permissions, thus inadvertently exposing the extended area's data to unauthorized reading.

It is for these reasons that <b>SetFileValidData</b> is not recommended for general purpose use, in addition to performance considerations, as discussed below.

For more information about security and access privileges, see 
<a href="/windows/desktop/SecBP/running-with-special-privileges">Running with Special Privileges</a> and <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

You can use the <b>SetFileValidData</b> function to  create large files in very specific circumstances so that the performance of subsequent file I/O can be better than other methods. Specifically, if the extended portion of the file is large and will be written to randomly, such as in a database type of application, the time it takes to extend and write to the file will be faster than using <a href="/windows/desktop/api/fileapi/nf-fileapi-setendoffile">SetEndOfFile</a> and writing randomly. In most other situations, there is usually no performance gain to using <b>SetFileValidData</b>, and sometimes there can be a performance penalty.

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

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setendoffile">SetEndOfFile</a>