---
UID: NF:fileapi.GetFileSizeEx
title: GetFileSizeEx function (fileapi.h)
description: Retrieves the size of the specified file.
helpviewer_keywords: ["GetFileSizeEx","GetFileSizeEx function [Files]","_win32_getfilesizeex","base.getfilesizeex","fileapi/GetFileSizeEx","fs.getfilesizeex","winbase/GetFileSizeEx"]
old-location: fs\getfilesizeex.htm
tech.root: fs
ms.assetid: 782457bc-8f37-4eec-8ff3-b148fd0a7345
ms.date: 12/05/2018
ms.keywords: GetFileSizeEx, GetFileSizeEx function [Files], _win32_getfilesizeex, base.getfilesizeex, fileapi/GetFileSizeEx, fs.getfilesizeex, winbase/GetFileSizeEx
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
 - GetFileSizeEx
 - fileapi/GetFileSizeEx
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
 - GetFileSizeEx
---

# GetFileSizeEx function


## -description

Retrieves the size of the specified file.

## -parameters

### -param hFile [in]

A handle to the file. The handle must have been created with the 
      <b>FILE_READ_ATTRIBUTES</b> access right or equivalent, or the caller must have sufficient permission on the directory that contains the file. 
      For more information, see 
      <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

### -param lpFileSize [out]

A pointer to a <a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a> structure that 
      receives the file size, in bytes.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

<b>Transacted Operations:  </b>If there is a transaction bound to the file handle, then the function returns information for the isolated 
      file view.

<b>Windows Store apps:  </b><b>GetFileSizeEx</b> is not supported. Use 
      <a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>.

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



<a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a>