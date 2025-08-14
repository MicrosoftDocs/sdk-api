---
UID: NF:winbase.GetFileInformationByHandleEx
title: GetFileInformationByHandleEx function (winbase.h)
description: Retrieves file information for the specified file. (GetFileInformationByHandleEx)
helpviewer_keywords: ["GetFileInformationByHandleEx","GetFileInformationByHandleEx function [Files]","fileextd/GetFileInformationByHandleEx","fs.getfileinformationbyhandleex","winbase/GetFileInformationByHandleEx"]
old-location: fs\getfileinformationbyhandleex.htm
tech.root: fs
ms.assetid: e261ea45-d084-490e-94b4-129bd76f6a04
ms.date: 12/05/2018
ms.keywords: GetFileInformationByHandleEx, GetFileInformationByHandleEx function [Files], fileextd/GetFileInformationByHandleEx, fs.getfileinformationbyhandleex, winbase/GetFileInformationByHandleEx
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib; FileExtd.lib on Windows Server 2003 and Windows XP
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows SDK on     Windows Server 2003 and Windows XP.
ms.custom: 19H1
f1_keywords:
 - GetFileInformationByHandleEx
 - winbase/GetFileInformationByHandleEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-file-l2-1-4.dll
 - api-ms-win-core-file-l2-1-3.dll
 - Kernel32.dll
 - API-MS-Win-Core-File-l2-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l2-1-1.dll
 - API-MS-Win-Core-File-l2-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
api_name:
 - GetFileInformationByHandleEx
---

# GetFileInformationByHandleEx function


## -description

Retrieves file information for the specified file.

For a more basic version of this function for desktop apps, see 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileinformationbyhandle">GetFileInformationByHandle</a>.

To set file information using a file handle, see 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>.

## -parameters

### -param hFile [in]

A handle to the file that contains the information to be retrieved.

This handle should not be a pipe handle.

### -param FileInformationClass [in]

A <a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a> enumeration 
       value that specifies the type of information to be retrieved.

For a table of valid values, see the Remarks section.

### -param lpFileInformation [out]

A pointer to the buffer that receives the requested file information. The structure that is returned 
      corresponds to the class that is specified by <i>FileInformationClass</i>. For a table of 
      valid structure types, see the Remarks section.

### -param dwBufferSize [in]

The size of the <i>lpFileInformation</i> buffer, in bytes.

## -returns

If the function succeeds, the return value is nonzero and file information data is contained in the buffer 
       pointed to by the <i>lpFileInformation</i> parameter.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If <i>FileInformationClass</i> is <b>FileStreamInfo</b> and the calls 
    succeed but no streams are returned, the error that is returned by 
    <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> is 
    <b>ERROR_HANDLE_EOF</b>.

Certain file information classes behave slightly differently on different operating system releases. These 
    classes are supported by the underlying drivers, and any information they return is subject to change between 
    operating system releases.

The following table shows the valid file information class types and their corresponding data structure types 
     for use with this function.

<table>
<tr>
<th><i>FileInformationClass</i> value</th>
<th><i>lpFileInformation</i> type</th>
</tr>
<tr>
<td><b>FileBasicInfo</b> (0)</td>
<td>
<a href="/windows/desktop/api/winbase/ns-winbase-file_basic_info">FILE_BASIC_INFO</a>
</td>
</tr>
<tr>
<td><b>FileStandardInfo</b> (1)</td>
<td>
<a href="/windows/desktop/api/winbase/ns-winbase-file_standard_info">FILE_STANDARD_INFO</a>
</td>
</tr>
<tr>
<td><b>FileNameInfo</b> (2)</td>
<td>
<a href="/windows/desktop/api/winbase/ns-winbase-file_name_info">FILE_NAME_INFO</a>
</td>
</tr>
<tr>
<td><b>FileStreamInfo</b> (7)</td>
<td>
<a href="/windows/desktop/api/winbase/ns-winbase-file_stream_info">FILE_STREAM_INFO</a>
</td>
</tr>
<tr>
<td><b>FileCompressionInfo</b> (8)</td>
<td>
<a href="/windows/desktop/api/winbase/ns-winbase-file_compression_info">FILE_COMPRESSION_INFO</a>
</td>
</tr>
<tr>
<td><b>FileAttributeTagInfo</b> (9)</td>
<td>
<a href="/windows/desktop/api/winbase/ns-winbase-file_attribute_tag_info">FILE_ATTRIBUTE_TAG_INFO</a>
</td>
</tr>
<tr>
<td><b>FileIdBothDirectoryInfo</b> (0xa)</td>
<td>
<a href="/windows/desktop/api/winbase/ns-winbase-file_id_both_dir_info">FILE_ID_BOTH_DIR_INFO</a>
</td>
</tr>
<tr>
<td><b>FileIdBothDirectoryRestartInfo</b> (0xb)</td>
<td>
<a href="/windows/desktop/api/winbase/ns-winbase-file_id_both_dir_info">FILE_ID_BOTH_DIR_INFO</a>
</td>
</tr>
<tr>
<td><b>FileRemoteProtocolInfo</b> (0xd)</td>
<td>
<a href="/windows/desktop/api/winbase/ns-winbase-file_remote_protocol_info">FILE_REMOTE_PROTOCOL_INFO</a>
</td>
</tr>
<tr>
<td><b>FileFullDirectoryInfo</b> (0xe)</td>
<td>
<a href="/windows/desktop/api/winbase/ns-winbase-file_full_dir_info">FILE_FULL_DIR_INFO</a>
</td>
</tr>
<tr>
<td><b>FileFullDirectoryRestartInfo</b> (0xf)</td>
<td>
<a href="/windows/desktop/api/winbase/ns-winbase-file_full_dir_info">FILE_FULL_DIR_INFO</a>
</td>
</tr>
<tr>
<td><b>FileStorageInfo</b> (0x10)</td>
<td>
<a href="/windows/desktop/api/winbase/ns-winbase-file_storage_info">FILE_STORAGE_INFO</a>
</td>
</tr>
<tr>
<td><b>FileAlignmentInfo</b> (0x11)</td>
<td>
<a href="/windows/desktop/api/winbase/ns-winbase-file_alignment_info">FILE_ALIGNMENT_INFO</a>
</td>
</tr>
<tr>
<td><b>FileIdInfo</b> (0x12)</td>
<td>
<a href="/windows/desktop/api/winbase/ns-winbase-file_id_info">FILE_ID_INFO</a>
</td>
</tr>
<tr>
<td><b>FileIdExtdDirectoryInfo</b> (0x13)</td>
<td>
<a href="/windows/desktop/api/winbase/ns-winbase-file_id_extd_dir_info">FILE_ID_EXTD_DIR_INFO</a>
</td>
</tr>
<tr>
<td><b>FileIdExtdDirectoryRestartInfo</b> (0x14)</td>
<td>
<a href="/windows/desktop/api/winbase/ns-winbase-file_id_extd_dir_info">FILE_ID_EXTD_DIR_INFO</a>
</td>
</tr>
</table>
 

<h3><a id="Transacted_Operations"></a><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
If there is a transaction bound to the thread at the time of the call, then the function returns the 
      compressed file size of the isolated file view. For more information, see 
      <a href="/windows/desktop/FileIO/about-transactional-ntfs">About Transactional NTFS</a>.

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

<a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileinformationbyhandle">SetFileInformationByHandle</a>
