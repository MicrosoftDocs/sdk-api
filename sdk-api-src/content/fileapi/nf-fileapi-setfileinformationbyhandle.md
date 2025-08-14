---
UID: NF:fileapi.SetFileInformationByHandle
title: SetFileInformationByHandle function (fileapi.h)
description: Sets the file information for the specified file.
helpviewer_keywords: ["SetFileInformationByHandle","SetFileInformationByHandle function [Files]","fileapi/SetFileInformationByHandle","fileextd/SetFileInformationByHandle","fs.setfileinformationbyhandle","winbase/SetFileInformationByHandle"]
old-location: fs\setfileinformationbyhandle.htm
tech.root: fs
ms.assetid: ea4981e6-a8f1-4977-aca9-b2f53604d449
ms.date: 12/05/2018
ms.keywords: SetFileInformationByHandle, SetFileInformationByHandle function [Files], fileapi/SetFileInformationByHandle, fileextd/SetFileInformationByHandle, fs.setfileinformationbyhandle, winbase/SetFileInformationByHandle
req.header: fileapi.h
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
 - SetFileInformationByHandle
 - fileapi/SetFileInformationByHandle
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
 - SetFileInformationByHandle
---

# SetFileInformationByHandle function


## -description

Sets the file information for the specified file.

To retrieve file information using a file handle, see 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileinformationbyhandle">GetFileInformationByHandle</a> or 
    <a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>.

## -parameters

### -param hFile [in]

A handle to the file for which to change information.

This handle must be opened with the appropriate permissions for the requested change. For more information, 
       see the Remarks and Example Code sections.

This handle should not be a pipe handle.

### -param FileInformationClass [in]

A <a href="/windows/desktop/api/minwinbase/ne-minwinbase-file_info_by_handle_class">FILE_INFO_BY_HANDLE_CLASS</a> enumeration 
       value that specifies the type of information to be changed.

For a table of valid values, see the Remarks section.

### -param lpFileInformation [in]

A pointer to the buffer that contains the information to change  for the specified file information class. 
       The structure that this parameter points to corresponds to the class that is specified by 
       <i>FileInformationClass</i>.

For a table of valid structure types, see the Remarks section.

### -param dwBufferSize [in]

The size of <i>lpFileInformation</i>, in bytes.

## -returns

Returns nonzero if successful or zero otherwise.

To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Certain file information classes behave slightly differently on different operating system releases. These 
    classes are supported by the underlying drivers, and any information they return is subject to change between 
    operating system releases.

The following table shows the valid file information classes and their corresponding data structure types for 
     use with this function.

<table>
<tr>
<th><i>FileInformationClass</i> value</th>
<th><i>lpFileInformation</i> type</th>
</tr>
<tr>
<td>
<b>FileBasicInfo</b>

0

</td>
<td>

<a href="/windows/desktop/api/winbase/ns-winbase-file_basic_info">FILE_BASIC_INFO</a>


</td>
</tr>
<tr>
<td>
<b>FileRenameInfo</b>

3

</td>
<td>

<a href="/windows/desktop/api/winbase/ns-winbase-file_rename_info">FILE_RENAME_INFO</a>


</td>
</tr>
<tr>
<td>
<b>FileDispositionInfo</b>

4

</td>
<td>

<a href="/windows/desktop/api/winbase/ns-winbase-file_disposition_info">FILE_DISPOSITION_INFO</a>


</td>
</tr>
<tr>
<td>
<b>FileAllocationInfo</b>

5

</td>
<td>

<a href="/windows/desktop/api/winbase/ns-winbase-file_allocation_info">FILE_ALLOCATION_INFO</a>


</td>
</tr>
<tr>
<td>
<b>FileEndOfFileInfo</b>

6

</td>
<td>

<a href="/windows/desktop/api/winbase/ns-winbase-file_end_of_file_info">FILE_END_OF_FILE_INFO</a>


</td>
</tr>
<tr>
<td>
<b>FileIoPriorityHintInfo</b>

12

</td>
<td>

<a href="/windows/desktop/api/winbase/ns-winbase-file_io_priority_hint_info">FILE_IO_PRIORITY_HINT_INFO</a>


</td>
</tr>
</table>
 

You must specify appropriate access flags when creating the file handle for use with 
    <b>SetFileInformationByHandle</b>. For example, if 
    the application is using <a href="/windows/desktop/api/winbase/ns-winbase-file_disposition_info">FILE_DISPOSITION_INFO</a> with 
    the <b>DeleteFile</b> member set to <b>TRUE</b>, the file would need 
    <b>DELETE</b> access requested in the call to the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function. To see an example of this, see the 
    Example Code section. For more information about file permissions, see 
    <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

If there is a transaction bound to the handle, then the changes made will be transacted for the information 
    classes <b>FileBasicInfo</b>, <b>FileRenameInfo</b>, 
    <b>FileAllocationInfo</b>, <b>FileEndOfFileInfo</b>, and 
    <b>FileDispositionInfo</b>. If <b>FileDispositionInfo</b> is specified, 
    only the delete operation is transacted if a <a href="/windows/desktop/api/fileapi/nf-fileapi-deletefilea">DeleteFile</a> 
    operation was requested. In this case, if the transaction is not committed before the handle is closed, the 
    deletion will not occur. For more information about TxF, see 
    <a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS (TxF)</a>.

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
See comment

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
See comment

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
 

SMB 3.0 does not support rename of alternate data streams on file shares with continuous availability capability.



#### Examples

The following C++ example shows how to create a file and mark it for deletion when the handle is closed.


```cpp
//...
  HANDLE hFile = CreateFile( TEXT("tempfile"), 
                             GENERIC_READ | GENERIC_WRITE | DELETE,
                             0 /* exclusive access */,
                             NULL, 
                             CREATE_ALWAYS,
                             0, 
                             NULL);

  if (hFile != INVALID_HANDLE_VALUE)
   {
    FILE_DISPOSITION_INFO fdi;
    fdi.DeleteFile = TRUE; // marking for deletion

    BOOL fResult = SetFileInformationByHandle( hFile, 
                                               FileDispositionInfo, 
                                               &fdi, 
                                               sizeof(FILE_DISPOSITION_INFO) );

    if (fResult)
     {
      // File will be deleted upon CloseHandle.
      _tprintf( TEXT("SetFileInformationByHandle marked tempfile for deletion\n") );

      // ... 
      // Now use the file for whatever temp data storage you need,
      // it will automatically be deleted upon CloseHandle or 
      // application termination.
      // ...
     }
    else
     {
      _tprintf( TEXT("error %lu:  SetFileInformationByHandle could not mark tempfile for deletion\n"), 
                GetLastError() );
     }

    CloseHandle(hFile); 

    // At this point, the file is closed and deleted by the system.
   }
  else 
   {
    _tprintf( TEXT("error %lu:  could not create tempfile\n"), 
              GetLastError() );
 }
//...

```

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>



<a href="/windows/desktop/SecAuthZ/generic-access-rights">Generic Access Rights</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfileinformationbyhandle">GetFileInformationByHandle</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileinformationbyhandleex">GetFileInformationByHandleEx</a>