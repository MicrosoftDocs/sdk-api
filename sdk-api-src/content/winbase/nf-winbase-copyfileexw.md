---
UID: NF:winbase.CopyFileExW
title: CopyFileExW function (winbase.h)
description: Copies an existing file to a new file, notifying the application of its progress through a callback function. (CopyFileExW)
helpviewer_keywords: ["COPY_FILE_ALLOW_DECRYPTED_DESTINATION", "COPY_FILE_COPY_SYMLINK", "COPY_FILE_FAIL_IF_EXISTS", "COPY_FILE_NO_BUFFERING", "COPY_FILE_OPEN_SOURCE_FOR_WRITE", "COPY_FILE_RESTARTABLE", "CopyFileEx", "CopyFileEx function [Files]", "CopyFileExW", "_win32_copyfileex", "base.copyfileex", "fs.copyfileex", "winbase/CopyFileEx", "winbase/CopyFileExW"]
old-location: fs\copyfileex.htm
tech.root: fs
ms.assetid: e19f0299-54fa-4e1e-855a-d2c71d29611b
ms.date: 12/05/2018
ms.keywords: COPY_FILE_ALLOW_DECRYPTED_DESTINATION, COPY_FILE_COPY_SYMLINK, COPY_FILE_FAIL_IF_EXISTS, COPY_FILE_NO_BUFFERING, COPY_FILE_OPEN_SOURCE_FOR_WRITE, COPY_FILE_RESTARTABLE, CopyFileEx, CopyFileEx function [Files], CopyFileExA, CopyFileExW, _win32_copyfileex, base.copyfileex, fs.copyfileex, winbase/CopyFileEx, winbase/CopyFileExA, winbase/CopyFileExW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CopyFileExW (Unicode) and CopyFileExA (ANSI)
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
 - CopyFileExW
 - winbase/CopyFileExW
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
 - API-Ms-Win-Core-File-Ansi-L2-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - CopyFileEx
 - CopyFileExA
 - CopyFileExW
---

# CopyFileExW function


## -description

Copies an existing file to a new file, notifying the application of its progress through a callback 
    function.

To perform this operation as a transacted operation, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-copyfiletransacteda">CopyFileTransacted</a> function.

## -parameters

### -param lpExistingFileName [in]

The name of an existing file.
      

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

If <i>lpExistingFileName</i> does not exist, the 
      <b>CopyFileEx</b> function fails, and the 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns 
      <b>ERROR_FILE_NOT_FOUND</b>.

### -param lpNewFileName [in]

The name of the new file.
      
By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param lpProgressRoutine [in, optional]

The address of a callback function of type <b>LPPROGRESS_ROUTINE</b> that is called 
      each time another portion of the file has been copied. This parameter can be <b>NULL</b>. For 
      more information on the progress callback function, see the 
      <a href="/windows/desktop/api/winbase/nc-winbase-lpprogress_routine">CopyProgressRoutine</a> function.

### -param lpData [in, optional]

The argument to be passed to the callback function. This parameter can be 
      <b>NULL</b>.

### -param pbCancel [in, optional]

If this flag is set to <b>TRUE</b> during the copy operation, the operation is canceled. 
      Otherwise, the copy operation will continue to completion.

### -param dwCopyFlags [in]

Flags that specify how the file is to be copied. This parameter can be a combination of the following 
      values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_ALLOW_DECRYPTED_DESTINATION"></a><a id="copy_file_allow_decrypted_destination"></a><dl>
<dt><b>COPY_FILE_ALLOW_DECRYPTED_DESTINATION</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
An attempt to copy an encrypted file will succeed even if the destination copy cannot be encrypted.

</td>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_COPY_SYMLINK"></a><a id="copy_file_copy_symlink"></a><dl>
<dt><b>COPY_FILE_COPY_SYMLINK</b></dt>
<dt>0x00000800</dt>
</dl>
</td>
<td width="60%">
If the source file is a symbolic link, the destination file is also a symbolic link pointing to the same 
        file that the source symbolic link is pointing to.
        

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_FAIL_IF_EXISTS"></a><a id="copy_file_fail_if_exists"></a><dl>
<dt><b>COPY_FILE_FAIL_IF_EXISTS</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
The copy operation fails immediately if the target file already exists.

</td>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_NO_BUFFERING"></a><a id="copy_file_no_buffering"></a><dl>
<dt><b>COPY_FILE_NO_BUFFERING</b></dt>
<dt>0x00001000</dt>
</dl>
</td>
<td width="60%">
The copy operation is performed using unbuffered I/O, bypassing system I/O cache resources. Recommended 
        for very large file transfers.
        

<b>Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_OPEN_SOURCE_FOR_WRITE"></a><a id="copy_file_open_source_for_write"></a><dl>
<dt><b>COPY_FILE_OPEN_SOURCE_FOR_WRITE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
The file is copied and the original file is opened for write access.

</td>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_RESTARTABLE"></a><a id="copy_file_restartable"></a><dl>
<dt><b>COPY_FILE_RESTARTABLE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Progress of the copy is tracked in the target file in case the copy fails. The failed copy can be 
        restarted at a later time by specifying the same values for <i>lpExistingFileName</i> and 
        <i>lpNewFileName</i> as those used in the call that failed. This can significantly slow 
        down the copy operation as the new file may be flushed multiple times during the copy operation.

</td>
</tr>
<tr>
<td width="40%"><a id="COPY_FILE_RESTARTABLE"></a><a id="copy_file_restartable"></a><dl>
<dt><b>COPY_FILE_REQUEST_COMPRESSED_TRAFFIC</b></dt>
<dt> 0x10000000</dt>
</dl>
</td>
<td width="60%">
<p>Request the underlying transfer channel compress the data during the copy operation. The request may not be supported for all mediums, in which case it is ignored. The compression attributes and parameters (computational complexity, memory usage) are not configurable through this API, and are subject to change between different OS releases.</p>
<p>This flag was introduced in Windows 10, version 1903 and Windows Server 2022. On Windows 10, the flag is supported for files residing on SMB shares, where the negotiated SMB protocol version is SMB v3.1.1 or greater.</p>
</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If <i>lpProgressRoutine</i> returns <b>PROGRESS_CANCEL</b> due to the 
       user canceling the operation, <b>CopyFileEx</b> will return zero 
       and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return 
       <b>ERROR_REQUEST_ABORTED</b>. In this case, the partially copied destination file is 
       deleted.

If <i>lpProgressRoutine</i> returns <b>PROGRESS_STOP</b> due to the 
       user stopping the operation, <b>CopyFileEx</b> will return zero 
       and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will return 
       <b>ERROR_REQUEST_ABORTED</b>. In this case, the partially copied destination file is left 
       intact.

## -remarks

This function preserves extended attributes, OLE structured storage, NTFS file system alternate data streams, 
     security resource attributes, and file attributes.

<b>Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>Security resource attributes (<b>ATTRIBUTE_SECURITY_INFORMATION</b>) for the existing file are not copied to the new file until Windows 8 
      and Windows Server 2012.

The security resource properties (<b>ATTRIBUTE_SECURITY_INFORMATION</b>) for the existing file are 
     copied to the new file.

<b>Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>Security resource properties for the existing file are not copied to the new file until 
      Windows 8 and Windows Server 2012.

This function fails with <b>ERROR_ACCESS_DENIED</b> if the destination file already exists 
    and has the <b>FILE_ATTRIBUTE_HIDDEN</b> or <b>FILE_ATTRIBUTE_READONLY</b> 
    attribute set.

When encrypted files are copied using <b>CopyFileEx</b>, the 
     function attempts to encrypt the destination file with the keys used in the encryption of the source file. If 
     this cannot be done, this function attempts to encrypt the destination file with default keys. If both of these 
     methods cannot be done, <b>CopyFileEx</b> fails with an 
     <b>ERROR_ENCRYPTION_FAILED</b> error code. If you want 
     <b>CopyFileEx</b> to complete the copy operation even if the 
     destination file cannot be encrypted, include the 
     <b>COPY_FILE_ALLOW_DECRYPTED_DESTINATION</b> as the value of the 
     <i>dwCopyFlags</i> parameter in your call to 
     <b>CopyFileEx</b>.


If <b>COPY_FILE_COPY_SYMLINK</b>  is specified, the following rules apply:

<ul>
<li>If the source file is a symbolic link, the symbolic link is copied, not the target file.</li>
<li>If the source file is not a symbolic link, there is no change in behavior.</li>
<li>If the destination file is an existing symbolic link, the symbolic link is overwritten, not the target 
       file.</li>
<li>If <b>COPY_FILE_FAIL_IF_EXISTS</b> is also specified, and the destination file is an 
       existing symbolic link, the operation fails in all cases.</li>
</ul>
If <b>COPY_FILE_COPY_SYMLINK</b> is not specified, the following rules apply:

<ul>
<li>If <b>COPY_FILE_FAIL_IF_EXISTS</b> is also specified, and the destination file is an 
       existing symbolic link, the operation fails only if the target of the symbolic link exists.</li>
<li>If <b>COPY_FILE_FAIL_IF_EXISTS</b> is not specified, there is no change in behavior.</li>
</ul>


<b>Windows 7, Windows Server 2008 R2, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>If you are writing an application that is optimizing file copy operations across a LAN, consider using the 
      <a href="/windows/desktop/api/mswsock/nf-mswsock-transmitfile">TransmitFile</a> function from Windows Sockets 
      (Winsock). <b>TransmitFile</b> supports high-performance 
      network transfers and provides a simple interface to send the contents of a file to a remote computer. To use 
      <b>TransmitFile</b>, you must write a Winsock client 
      application that sends the file from the source computer as well as a Winsock server application that uses 
      other Winsock functions to receive the file on the remote computer.

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
 





> [!NOTE]
> The winbase.h header defines CopyFileEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-copyfile">CopyFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-copyfiletransacteda">CopyFileTransacted</a>



<a href="/windows/desktop/api/winbase/nc-winbase-lpprogress_routine">CopyProgressRoutine</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-movefile">MoveFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-movefilewithprogressa">MoveFileWithProgress</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>



<a href="/windows/desktop/api/mswsock/nf-mswsock-transmitfile">TransmitFile</a>
