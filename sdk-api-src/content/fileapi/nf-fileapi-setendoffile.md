---
UID: NF:fileapi.SetEndOfFile
title: SetEndOfFile function (fileapi.h)
description: Sets the physical file size for the specified file to the current position of the file pointer.
helpviewer_keywords: ["SetEndOfFile","SetEndOfFile function [Files]","_win32_setendoffile","base.setendoffile","fileapi/SetEndOfFile","fs.setendoffile","winbase/SetEndOfFile"]
old-location: fs\setendoffile.htm
tech.root: fs
ms.assetid: 2a579609-144a-4b77-8605-87aecf1f0957
ms.date: 12/05/2018
ms.keywords: SetEndOfFile, SetEndOfFile function [Files], _win32_setendoffile, base.setendoffile, fileapi/SetEndOfFile, fs.setendoffile, winbase/SetEndOfFile
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - SetEndOfFile
 - fileapi/SetEndOfFile
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
 - SetEndOfFile
---

# SetEndOfFile function


## -description

Sets the physical file size for the specified file to the current position of the file pointer.

The physical file size is also referred to as the end of the file. The <b>SetEndOfFile</b> function can be used to truncate or extend a file. To set the logical end of a file, use the <a href="/windows/desktop/api/fileapi/nf-fileapi-setfilevaliddata">SetFileValidData</a> function.

## -parameters

### -param hFile [in]

A handle to the file to be extended or truncated.

 The file handle must be created with the <b>GENERIC_WRITE</b> access right. For more information, see 
<a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>SetEndOfFile</b> function can be used to truncate or extend a file. If the file is extended, the contents of the file between the old end of the file  and the new  end of the file are not defined.

Each file stream has the following:

<ul>
<li>File size: the size of the data in a file, to the byte.</li>
<li>Allocation size: the size of the space that is allocated for a file on a disk, which is always an even multiple of the cluster size.</li>
<li>Valid data length: the length of the data in a file that is actually written, to the byte. This value is always less than or equal to the file size.</li>
</ul>
  The <b>SetEndOfFile</b> function sets the file size. Use <a href="/windows/desktop/api/fileapi/nf-fileapi-setfilevaliddata">SetFileValidData</a> to set the valid data length. 

If  
<a href="/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a> is called to create a file mapping object for <i>hFile</i>, <a href="/windows/desktop/api/memoryapi/nf-memoryapi-unmapviewoffile">UnmapViewOfFile</a> must be called first to unmap all views and call 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> to close the file mapping object before you can call 
<b>SetEndOfFile</b>.

<h3><a id="Transacted_Operations"></a><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
If there is a transaction bound to the handle, then the change in the end-of-file position is transacted.

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

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createfilemappinga">CreateFileMapping</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfilevaliddata">SetFileValidData</a>



<a href="/windows/desktop/api/memoryapi/nf-memoryapi-unmapviewoffile">UnmapViewOfFile</a>