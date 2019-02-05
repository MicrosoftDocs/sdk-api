---
UID: NE:minwinbase._FILE_INFO_BY_HANDLE_CLASS
title: FILE_INFO_BY_HANDLE_CLASS
author: windows-sdk-content
description: Identifies the type of file information that GetFileInformationByHandleEx should retrieve or SetFileInformationByHandle should set.
old-location: fs\file_info_by_handle_class.htm
tech.root: FileIO
ms.assetid: 8f02e824-ca41-48c1-a5e8-5b12d81886b5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PFILE_INFO_BY_HANDLE_CLASS, FILE_INFO_BY_HANDLE_CLASS, FILE_INFO_BY_HANDLE_CLASS enumeration [Files], FileAlignmentInfo, FileAllocationInfo, FileAttributeTagInfo, FileBasicInfo, FileCompressionInfo, FileDispositionInfo, FileEndOfFileInfo, FileFullDirectoryInfo, FileFullDirectoryRestartInfo, FileIdBothDirectoryInfo, FileIdBothDirectoryRestartInfo, FileIdExtdDirectoryInfo, FileIdExtdDirectoryRestartInfo, FileIdInfo, FileIoPriorityHintInfo, FileNameInfo, FileRemoteProtocolInfo, FileRenameInfo, FileStandardInfo, FileStorageInfo, FileStreamInfo, MaximumFileInfoByHandlesClass, PFILE_INFO_BY_HANDLE_CLASS, PFILE_INFO_BY_HANDLE_CLASS enumeration pointer [Files], fileextd/FILE_INFO_BY_HANDLE_CLASS, fileextd/FileAlignmentInfo, fileextd/FileAllocationInfo, fileextd/FileAttributeTagInfo, fileextd/FileBasicInfo, fileextd/FileCompressionInfo, fileextd/FileDispositionInfo, fileextd/FileEndOfFileInfo, fileextd/FileFullDirectoryInfo, fileextd/FileFullDirectoryRestartInfo, fileextd/FileIdBothDirectoryInfo, fileextd/FileIdBothDirectoryRestartInfo, fileextd/FileIdExtdDirectoryInfo, fileextd/FileIdExtdDirectoryRestartInfo, fileextd/FileIdInfo, fileextd/FileIoPriorityHintInfo, fileextd/FileNameInfo, fileextd/FileRemoteProtocolInfo, fileextd/FileRenameInfo, fileextd/FileStandardInfo, fileextd/FileStorageInfo, fileextd/FileStreamInfo, fileextd/MaximumFileInfoByHandlesClass, fileextd/PFILE_INFO_BY_HANDLE_CLASS, fs.file_info_by_handle_class, minwinbase/FILE_INFO_BY_HANDLE_CLASS, minwinbase/FileAlignmentInfo, minwinbase/FileAllocationInfo, minwinbase/FileAttributeTagInfo, minwinbase/FileBasicInfo, minwinbase/FileCompressionInfo, minwinbase/FileDispositionInfo, minwinbase/FileEndOfFileInfo, minwinbase/FileFullDirectoryInfo, minwinbase/FileFullDirectoryRestartInfo, minwinbase/FileIdBothDirectoryInfo, minwinbase/FileIdBothDirectoryRestartInfo, minwinbase/FileIdExtdDirectoryInfo, minwinbase/FileIdExtdDirectoryRestartInfo, minwinbase/FileIdInfo, minwinbase/FileIoPriorityHintInfo, minwinbase/FileNameInfo, minwinbase/FileRemoteProtocolInfo, minwinbase/FileRenameInfo, minwinbase/FileStandardInfo, minwinbase/FileStorageInfo, minwinbase/FileStreamInfo, minwinbase/MaximumFileInfoByHandlesClass, minwinbase/PFILE_INFO_BY_HANDLE_CLASS"
ms.topic: enum
req.header: minwinbase.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MinWinBase.h
 - FileExtd.h
api_name:
 - FILE_INFO_BY_HANDLE_CLASS
product: Windows
targetos: Windows
req.typenames: FILE_INFO_BY_HANDLE_CLASS, *PFILE_INFO_BY_HANDLE_CLASS
req.redist: Windows SDK on     Windows Server 2003 and Windows XP.
---

# FILE_INFO_BY_HANDLE_CLASS enumeration


## -description


Identifies the type  of file information that 
   <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a> should retrieve 
   or <a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a> should 
   set.


## -enum-fields




### -field FileBasicInfo

Minimal information for the file should be retrieved or set. Used for file handles. See 
      <a href="https://msdn.microsoft.com/7765e430-cf6b-4ccf-b5e7-9fb6e15ca6d6">FILE_BASIC_INFO</a>.


### -field FileStandardInfo

Extended information for the file should be retrieved. Used for file handles. Use only when calling 
      <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>. See 
      <a href="https://msdn.microsoft.com/da3187de-7de2-4307-a083-ae5fff6d8096">FILE_STANDARD_INFO</a>.


### -field FileNameInfo

The file name should be retrieved. Used for any handles. Use only when calling 
      <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>. See 
      <a href="https://msdn.microsoft.com/7ab98f41-b99e-4731-b803-921064a961c4">FILE_NAME_INFO</a>.


### -field FileRenameInfo

The file name should be changed. Used for file handles. Use only when calling 
      <a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>. See 
      <a href="https://msdn.microsoft.com/f4de0130-66fd-4847-bb6f-3f16fe17ca6e">FILE_RENAME_INFO</a>.


### -field FileDispositionInfo

The file should be deleted. Used for any handles. Use only when calling 
      <a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>. See 
      <a href="https://msdn.microsoft.com/07095f62-323a-463a-a33e-7e4ca9adcb69">FILE_DISPOSITION_INFO</a>.


### -field FileAllocationInfo

The file allocation information should be changed. Used for file handles. Use only when calling 
      <a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>. See 
      <a href="https://msdn.microsoft.com/909f1747-0099-407e-89a7-bec6331887da">FILE ALLOCATION INFO</a>.


### -field FileEndOfFileInfo

The end of the file should be set. Use only when calling 
      <a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>. See 
      <a href="https://msdn.microsoft.com/77500ae7-654a-4b34-aaee-5c3844303271">FILE_END_OF_FILE_INFO</a>.


### -field FileStreamInfo

File stream information for the specified file should be retrieved. Used for any handles. Use only when calling 
      <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>. See 
      <a href="https://msdn.microsoft.com/36d1b0b3-bd6b-41e7-937a-4e8deef6f9da">FILE_STREAM_INFO</a>.


### -field FileCompressionInfo

File compression information should be retrieved. Used for any handles. Use only when calling 
      <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>. See 
      <a href="https://msdn.microsoft.com/2f64e7cc-e23c-4e3d-8e17-0e8e38f1ea24">FILE_COMPRESSION_INFO</a>.


### -field FileAttributeTagInfo

File attribute information should be retrieved. Used for any handles. Use only when calling 
      <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>. See 
      <a href="https://msdn.microsoft.com/4a2467a2-c22a-4ee6-a40e-5603ea381adc">FILE_ATTRIBUTE_TAG_INFO</a>.


### -field FileIdBothDirectoryInfo

Files in the specified directory should be retrieved. Used for directory handles. Use only when calling 
      <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>. The number 
      of files returned for each call to 
      <b>GetFileInformationByHandleEx</b> depends on 
      the size of the buffer that is passed to the function. Any subsequent calls to 
      <b>GetFileInformationByHandleEx</b> on the same 
      handle will resume the enumeration operation after the last file is returned. See 
      <a href="https://msdn.microsoft.com/d7011ea4-e70a-4c03-a715-6144ce0c7029">FILE_ID_BOTH_DIR_INFO</a>.


### -field FileIdBothDirectoryRestartInfo

Identical to <b>FileIdBothDirectoryInfo</b>, but forces the enumeration operation to 
      start again from the beginning. See 
      <a href="https://msdn.microsoft.com/d7011ea4-e70a-4c03-a715-6144ce0c7029">FILE_ID_BOTH_DIR_INFO</a>.


### -field FileIoPriorityHintInfo

Priority hint information should be  set. Use only when calling 
      <a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>. See 
      <a href="https://msdn.microsoft.com/a142b8fd-b71c-4449-a8c6-fb23715d1576">FILE_IO_PRIORITY_HINT_INFO</a>.


### -field FileRemoteProtocolInfo

File remote protocol information should be retrieved. Use for any handles. Use only when calling 
      <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>. See 
      <a href="https://msdn.microsoft.com/ddb555ad-0acb-4538-88ce-a871adfc21fc">FILE_REMOTE_PROTOCOL_INFO</a>.


### -field FileFullDirectoryInfo

Files in the specified directory should be retrieved. Used for directory handles. Use only when calling 
       <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>. See 
       <a href="https://msdn.microsoft.com/606726e7-fd6b-4419-bd37-7282283007f8">FILE_FULL_DIR_INFO</a>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows 8 and Windows Server 2012


### -field FileFullDirectoryRestartInfo

Identical to <b>FileFullDirectoryInfo</b>, but forces the enumeration operation to 
       start again from the beginning. Use only when calling 
       <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>. See 
       <a href="https://msdn.microsoft.com/606726e7-fd6b-4419-bd37-7282283007f8">FILE_FULL_DIR_INFO</a>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows 8 and Windows Server 2012


### -field FileStorageInfo

File storage information should be retrieved. Use for any handles. Use only when calling 
       <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>. See 
       <a href="https://msdn.microsoft.com/1aa9585d-9001-4d94-babe-a39c8dde2332">FILE_STORAGE_INFO</a>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows 8 and Windows Server 2012


### -field FileAlignmentInfo

File alignment information should be retrieved. Use for any handles. Use only when calling 
       <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>. See 
       <a href="https://msdn.microsoft.com/a6d3cba0-d59b-45c2-a763-ecdde5b36348">FILE_ALIGNMENT_INFO</a>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows 8 and Windows Server 2012


### -field FileIdInfo

File information should be retrieved. Use for any handles. Use only when calling 
       <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>. See 
       <a href="https://msdn.microsoft.com/e2774e29-1a90-44d6-9001-f73a98be6624">FILE_ID_INFO</a>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows 8 and Windows Server 2012


### -field FileIdExtdDirectoryInfo

Files in the specified directory should be retrieved. Used for directory handles. Use only when calling 
       <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>. See 
       <a href="https://msdn.microsoft.com/68f222c4-beb6-4be1-a31a-c5fbebbf76f7">FILE_ID_EXTD_DIR_INFO</a>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows 8 and Windows Server 2012


### -field FileIdExtdDirectoryRestartInfo

Identical to <b>FileIdExtdDirectoryInfo</b>, but forces the enumeration operation to 
       start again from the beginning. Use only when calling 
       <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>. See 
       <a href="https://msdn.microsoft.com/68f222c4-beb6-4be1-a31a-c5fbebbf76f7">FILE_ID_EXTD_DIR_INFO</a>.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported before Windows 8 and Windows Server 2012


### -field FileDispositionInfoEx


### -field FileRenameInfoEx


### -field MaximumFileInfoByHandleClass




#### - MaximumFileInfoByHandlesClass

This value is used for validation. Supported values are less than this value.


## -remarks



As noted in the preceding section, some file information classes are valid only for use with 
    <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>. Others are 
    valid only for use with 
    <a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>. Where neither 
    function is mentioned, the information class is valid with both functions.




## -see-also




<a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>



<a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>
 

 

