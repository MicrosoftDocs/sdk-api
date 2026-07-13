---
UID: NF:fileapi.SetFilePointerEx
title: SetFilePointerEx function (fileapi.h)
description: Moves the file pointer of the specified file. (SetFilePointerEx)
helpviewer_keywords: ["FILE_BEGIN","FILE_CURRENT","FILE_END","SetFilePointerEx","SetFilePointerEx function [Files]","_win32_setfilepointerex","base.setfilepointerex","fileapi/SetFilePointerEx","fs.setfilepointerex","winbase/SetFilePointerEx"]
old-location: fs\setfilepointerex.htm
tech.root: fs
ms.assetid: a6fdfa00-626d-425d-b00e-c174b19ea4b9
ms.date: 12/05/2018
ms.keywords: FILE_BEGIN, FILE_CURRENT, FILE_END, SetFilePointerEx, SetFilePointerEx function [Files], _win32_setfilepointerex, base.setfilepointerex, fileapi/SetFilePointerEx, fs.setfilepointerex, winbase/SetFilePointerEx
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
 - SetFilePointerEx
 - fileapi/SetFilePointerEx
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
 - SetFilePointerEx
---

# SetFilePointerEx function


## -description

Moves the file pointer of the specified file.

## -parameters

### -param hFile [in]

A handle to the file. The file handle must have been created with the 
      <b>GENERIC_READ</b> or <b>GENERIC_WRITE</b> access right. For more 
      information, see 
      <a href="/windows/desktop/FileIO/file-security-and-access-rights">File Security and Access Rights</a>.

### -param liDistanceToMove [in]

The number of bytes to move the file pointer. A positive value moves the pointer forward in the file and a 
      negative value moves the file pointer backward.

### -param lpNewFilePointer [out, optional]

A pointer to a variable to receive the new file pointer. If this parameter is 
      <b>NULL</b>, the new file pointer is not returned.

### -param dwMoveMethod [in]

The starting point for the file pointer move. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_BEGIN"></a><a id="file_begin"></a><dl>
<dt><b>FILE_BEGIN</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The starting point is zero or the beginning of the file. If this flag is specified, then the 
        <i>liDistanceToMove</i> parameter is interpreted as an unsigned value.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_CURRENT"></a><a id="file_current"></a><dl>
<dt><b>FILE_CURRENT</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The start point is the current value of the file pointer.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_END"></a><a id="file_end"></a><dl>
<dt><b>FILE_END</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The starting point is the current end-of-file position.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The file pointer returned by this function is not used for overlapped read and write operations. To specify 
    the offset for overlapped operations, use the <b>Offset</b> and 
    <b>OffsetHigh</b> members of the 
    <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure.

You cannot use the <b>SetFilePointerEx</b> function with a handle to a nonseeking 
    device such as a pipe or a communications device. To determine the file type for <i>hFile</i>, 
    use the <a href="/windows/desktop/api/fileapi/nf-fileapi-getfiletype">GetFileType</a> function.

Use caution when setting the file pointer in a multithreaded application. You must synchronize access to 
    shared resources. For example, an application whose threads share a file handle, update the file pointer, and read 
    from the file must protect this sequence by using a critical section object or a mutex object. For more 
    information about these objects, see 
    <a href="/windows/desktop/Sync/critical-section-objects">Critical Section Objects</a> 
    and <a href="/windows/desktop/Sync/mutex-objects">Mutex Objects</a>.

If the <i>hFile</i> handle was opened with the 
    <b>FILE_FLAG_NO_BUFFERING</b> flag set, an application can move the file pointer only to 
    sector-aligned positions. A sector-aligned position is a position that is a whole number multiple of the volume's 
    sector size. An application can obtain a volume's sector size by calling the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespacea">GetDiskFreeSpace</a> function. If an application 
    calls <b>SetFilePointerEx</b> with distance-to-move values that result in a position 
    that is not sector-aligned and a handle that was opened with <b>FILE_FLAG_NO_BUFFERING</b>, the 
    function fails, and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
    <b>ERROR_INVALID_PARAMETER</b>. For additional information, see 
    <a href="/windows/desktop/FileIO/file-buffering">File Buffering</a>.

Note that it is not an error to set the file pointer to a position beyond the end of the file. The size of the 
    file does not increase until you call the <a href="/windows/desktop/api/fileapi/nf-fileapi-setendoffile">SetEndOfFile</a>, 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>, or 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a> function. A write operation increases the size 
    of the file to the file pointer position plus the size of the buffer written, which results in the intervening 
    bytes being zero initialized.

You can use <b>SetFilePointerEx</b> to determine the length of a file. To do this, 
    use <b>FILE_END</b> for <i>dwMoveMethod</i> and seek to location zero. The 
    file offset returned is the length of the file. However, this practice can have unintended side effects, such as 
    failure to save the current file pointer so that the program can return to that location. It is simpler and safer 
    to use the <a href="/windows/desktop/api/fileapi/nf-fileapi-getfilesizeex">GetFileSizeEx</a> function instead.

You can also use <b>SetFilePointerEx</b> to query the current file pointer position. 
    To do this, specify a move method of <b>FILE_CURRENT</b> and a distance of zero.

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



<a href="/windows/desktop/api/fileapi/nf-fileapi-getdiskfreespaceexa">GetDiskFreeSpaceEx</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfilesizeex">GetFileSizeEx</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfiletype">GetFileType</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setendoffile">SetEndOfFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefileex">WriteFileEx</a>
