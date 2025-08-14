---
UID: NF:fileapi.GetFileInformationByHandle
title: GetFileInformationByHandle function (fileapi.h)
description: Retrieves file information for the specified file. (GetFileInformationByHandle)
helpviewer_keywords: ["GetFileInformationByHandle","GetFileInformationByHandle function [Files]","_win32_getfileinformationbyhandle","base.getfileinformationbyhandle","fileapi/GetFileInformationByHandle","fs.getfileinformationbyhandle","winbase/GetFileInformationByHandle"]
old-location: fs\getfileinformationbyhandle.htm
tech.root: fs
ms.assetid: d026ee3a-c165-42a2-a4e1-efccdafbefc5
ms.date: 12/05/2018
ms.keywords: GetFileInformationByHandle, GetFileInformationByHandle function [Files], _win32_getfileinformationbyhandle, base.getfileinformationbyhandle, fileapi/GetFileInformationByHandle, fs.getfileinformationbyhandle, winbase/GetFileInformationByHandle
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
 - GetFileInformationByHandle
 - fileapi/GetFileInformationByHandle
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
 - GetFileInformationByHandle
---

# GetFileInformationByHandle function


## -description

Retrieves file information for the specified file.

For a more advanced version of this function, see 
    <a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>.

To set file information using a file handle, see 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>.

## -parameters

### -param hFile [in]

A handle to the file that contains the information to be retrieved.

This handle should not be a pipe handle.

### -param lpFileInformation [out]

A pointer to a 
      <a href="/windows/desktop/api/fileapi/ns-fileapi-by_handle_file_information">BY_HANDLE_FILE_INFORMATION</a> structure that 
      receives the file information.

## -returns

If the function succeeds, the return value is nonzero and file information data is contained in the buffer 
       pointed to by the <i>lpFileInformation</i> parameter.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Depending on the underlying network features of the operating system and the type of server connected to, the 
    <b>GetFileInformationByHandle</b> function may fail, 
    return partial information, or full information for the given file.

You can compare the <b>VolumeSerialNumber</b> and <b>FileIndex</b> 
    members returned in the 
    <a href="/windows/desktop/api/fileapi/ns-fileapi-by_handle_file_information">BY_HANDLE_FILE_INFORMATION</a> structure to 
    determine if two paths map to the same target; for example, you can compare two file paths and determine if they 
    map to the same directory.

IIn Windows 8 and Windows Server 2012, this function is supported by the following technologies.

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
 

<h3><a id="Transacted_Operations"></a><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
If there is a transaction bound to the thread at the time of the call, then the function returns the 
      compressed file size of the isolated file view. For more information, see 
      <a href="/windows/desktop/FileIO/about-transactional-ntfs">About Transactional NTFS</a>.

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>
