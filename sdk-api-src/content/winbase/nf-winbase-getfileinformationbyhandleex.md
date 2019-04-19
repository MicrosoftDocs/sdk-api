---
UID: NF:winbase.GetFileInformationByHandleEx
title: GetFileInformationByHandleEx function (winbase.h)
author: windows-sdk-content
description: Retrieves file information for the specified file.
old-location: fs\getfileinformationbyhandleex.htm
tech.root: FileIO
ms.assetid: e261ea45-d084-490e-94b4-129bd76f6a04
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFileInformationByHandleEx, GetFileInformationByHandleEx function [Files], fileextd/GetFileInformationByHandleEx, fs.getfileinformationbyhandleex, winbase/GetFileInformationByHandleEx
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-File-l2-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l2-1-1.dll
 - API-MS-Win-Core-File-l2-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
api_name:
 - GetFileInformationByHandleEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows SDK on     Windows Server 2003 and Windows XP.
ms.custom: 19H1
---

# GetFileInformationByHandleEx function


## -description


Retrieves file information for the specified file.

For a more basic version of this function for desktop apps, see 
    <a href="https://msdn.microsoft.com/d026ee3a-c165-42a2-a4e1-efccdafbefc5">GetFileInformationByHandle</a>.

To set file information using a file handle, see 
    <a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>.


## -parameters




### -param hFile [in]

A handle to the file that contains the information to be retrieved.

This handle should not be a pipe handle.


### -param FileInformationClass [in]

A <a href="https://msdn.microsoft.com/8f02e824-ca41-48c1-a5e8-5b12d81886b5">FILE_INFO_BY_HANDLE_CLASS</a> enumeration 
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
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If <i>FileInformationClass</i> is <b>FileStreamInfo</b> and the calls 
    succeed but no streams are returned, the error that is returned by 
    <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> is 
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
<a href="https://msdn.microsoft.com/7765e430-cf6b-4ccf-b5e7-9fb6e15ca6d6">FILE_BASIC_INFO</a>
</td>
</tr>
<tr>
<td><b>FileStandardInfo</b> (1)</td>
<td>
<a href="https://msdn.microsoft.com/da3187de-7de2-4307-a083-ae5fff6d8096">FILE_STANDARD_INFO</a>
</td>
</tr>
<tr>
<td><b>FileNameInfo</b> (2)</td>
<td>
<a href="https://msdn.microsoft.com/7ab98f41-b99e-4731-b803-921064a961c4">FILE_NAME_INFO</a>
</td>
</tr>
<tr>
<td><b>FileStreamInfo</b> (7)</td>
<td>
<a href="https://msdn.microsoft.com/36d1b0b3-bd6b-41e7-937a-4e8deef6f9da">FILE_STREAM_INFO</a>
</td>
</tr>
<tr>
<td><b>FileCompressionInfo</b> (8)</td>
<td>
<a href="https://msdn.microsoft.com/2f64e7cc-e23c-4e3d-8e17-0e8e38f1ea24">FILE_COMPRESSION_INFO</a>
</td>
</tr>
<tr>
<td><b>FileAttributeTagInfo</b> (9)</td>
<td>
<a href="https://msdn.microsoft.com/4a2467a2-c22a-4ee6-a40e-5603ea381adc">FILE_ATTRIBUTE_TAG_INFO</a>
</td>
</tr>
<tr>
<td><b>FileIdBothDirectoryInfo</b> (0xa)</td>
<td>
<a href="https://msdn.microsoft.com/d7011ea4-e70a-4c03-a715-6144ce0c7029">FILE_ID_BOTH_DIR_INFO</a>
</td>
</tr>
<tr>
<td><b>FileIdBothDirectoryRestartInfo</b> (0xb)</td>
<td>
<a href="https://msdn.microsoft.com/d7011ea4-e70a-4c03-a715-6144ce0c7029">FILE_ID_BOTH_DIR_INFO</a>
</td>
</tr>
<tr>
<td><b>FileRemoteProtocolInfo</b> (0xd)</td>
<td>
<a href="https://msdn.microsoft.com/ddb555ad-0acb-4538-88ce-a871adfc21fc">FILE_REMOTE_PROTOCOL_INFO</a>
</td>
</tr>
<tr>
<td><b>FileFullDirectoryInfo</b> (0xe)</td>
<td>
<a href="https://msdn.microsoft.com/606726e7-fd6b-4419-bd37-7282283007f8">FILE_FULL_DIR_INFO</a>
</td>
</tr>
<tr>
<td><b>FileFullDirectoryRestartInfo</b> (0xf)</td>
<td>
<a href="https://msdn.microsoft.com/606726e7-fd6b-4419-bd37-7282283007f8">FILE_FULL_DIR_INFO</a>
</td>
</tr>
<tr>
<td><b>FileStorageInfo</b> (0x10)</td>
<td>
<a href="https://msdn.microsoft.com/1aa9585d-9001-4d94-babe-a39c8dde2332">FILE_STORAGE_INFO</a>
</td>
</tr>
<tr>
<td><b>FileAlignmentInfo</b> (0x11)</td>
<td>
<a href="https://msdn.microsoft.com/a6d3cba0-d59b-45c2-a763-ecdde5b36348">FILE_ALIGNMENT_INFO</a>
</td>
</tr>
<tr>
<td><b>FileIdInfo</b> (0x12)</td>
<td>
<a href="https://msdn.microsoft.com/e2774e29-1a90-44d6-9001-f73a98be6624">FILE_ID_INFO</a>
</td>
</tr>
<tr>
<td><b>FileIdExtdDirectoryInfo</b> (0x13)</td>
<td>
<a href="https://msdn.microsoft.com/68f222c4-beb6-4be1-a31a-c5fbebbf76f7">FILE_ID_EXTD_DIR_INFO</a>
</td>
</tr>
<tr>
<td><b>FileIdExtdDirectoryRestartInfo</b> (0x14)</td>
<td>
<a href="https://msdn.microsoft.com/68f222c4-beb6-4be1-a31a-c5fbebbf76f7">FILE_ID_EXTD_DIR_INFO</a>
</td>
</tr>
</table>
 

<h3><a id="Transacted_Operations"></a><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
If there is a transaction bound to the thread at the time of the call, then the function returns the 
      compressed file size of the isolated file view. For more information, see 
      <a href="https://msdn.microsoft.com/52341315-0412-4a87-aca0-9adea7aae62f">About Transactional NTFS</a>.

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




<a href="https://msdn.microsoft.com/8f02e824-ca41-48c1-a5e8-5b12d81886b5">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>
 

 

