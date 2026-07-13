---
UID: NF:fileapifromapp.CreateFile2FromAppW
tech.root: fs
title: CreateFile2FromAppW
ms.date: 03/23/2021
targetos: Windows
description: Creates or opens a file or I/O device. The behavior of this function is identical to CreateFile2, except that this function adheres to the Universal Windows Platform app security model.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: fileapifromapp.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: OneCore.Lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10, version 1803
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_location:
- Kernel32.dll
- sqlite.dll
- api-ms-win-core-file-fromapp-l1-1-0.dll
api_name:
- CreateFile2FromAppW
- CreateFile2FromApp
api_type:
- DLLExport
f1_keywords:
 - CreateFile2FromAppW
 - fileapifromapp/CreateFile2FromAppW
dev_langs:
 - c++
---

## -description

Creates or opens a file or I/O device. The behavior of this function is identical to [**CreateFile2**](../fileapi/nf-fileapi-createfile2.md), except that this function adheres to the Universal Windows Platform app security model.


## -parameters

### -param lpFileName

The name of the file or device to be created or opened.
    
For information on special device names, see [Defining an MS-DOS Device Name](/windows/win32/fileio/defining-an-ms-dos-device-name).
    
To create a file stream, specify the name of the file, a colon, and then the name of the stream. For more information, see [File Streams](/windows/win32/fileio/file-streams).
    
For information about opting out of the **MAX\_PATH** limitation without prepending "\\\\?\\", see the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param dwDesiredAccess

The requested access to the file or device, which can be summarized as read, write, both or neither zero).

The most commonly used values are **GENERIC\_READ**, **GENERIC\_WRITE**, or both (`GENERIC_READ | GENERIC_WRITE`). For more information, see [Generic Access Rights](/windows/win32/secauthz/generic-access-rights), [File Security and Access Rights](/windows/win32/fileio/file-security-and-access-rights), [**File Access Rights Constants**](/windows/win32/fileio/file-access-rights-constants), and [**ACCESS\_MASK**](/windows/win32/secauthz/access-mask).

If this parameter is zero, the application can query certain metadata such as file, directory, or device attributes without accessing that file or device, even if **GENERIC\_READ** access would have been denied.

You cannot request an access mode that conflicts with the sharing mode that is specified by the *dwShareMode* parameter in an open request that already has an open handle.


### -param dwShareMode

The requested sharing mode of the file or device, which can be read, write, both, delete, all of these, or none (refer to the following table). Access requests to attributes or extended attributes are not affected by this flag.
    
If this parameter is zero and the function succeeds, the file or device cannot be shared and cannot be opened again until the handle to the file or device is closed. For more information, see the Remarks section.

You can't request a sharing mode that conflicts with the access mode that is specified in an existing request that has an open handle. This function would fail and the [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md) function would return **ERROR\_SHARING\_VIOLATION**.

To enable a process to share a file or device while another process has the file or device open, use a compatible combination of one or more of the following values. For more information about valid combinations of this parameter with the *dwDesiredAccess* parameter, see [Creating and Opening Files](/windows/win32/fileio/creating-and-opening-files).

**Note**  The sharing options for each open handle remain in effect until that handle is closed, regardless of process context.

 

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="0"></span>
<strong>0</strong>
0x00000000</td>
<td><p>Prevents other processes from opening a file or device if they request delete, read, or write access. Exclusive access to a file or directory is only granted if the application has write access to the file.</p></td>
</tr>
<tr class="even">
<td><span id="FILE_SHARE_DELETE"></span><span id="file_share_delete"></span>
<strong>FILE_SHARE_DELETE</strong>
0x00000004</td>
<td><p>Enables subsequent open operations on a file or device to request delete access.</p>
<p>Otherwise, other processes cannot open the file or device if they request delete access.</p>
<p>If this flag is not specified, but the file or device has been opened for delete access, the function fails.</p>
<strong>Note</strong>  Delete access allows both delete and rename operations.
<div>
 
</div></td>
</tr>
<tr class="odd">
<td><span id="FILE_SHARE_READ"></span><span id="file_share_read"></span>
<strong>FILE_SHARE_READ</strong>
0x00000001</td>
<td><p>Enables subsequent open operations on a file or device to request read access.</p>
<p>Otherwise, other processes cannot open the file or device if they request read access.</p>
<p>If this flag is not specified, but the file or device has been opened for read access, the function fails.</p>
<p>If a file or directory is being opened and this flag is not specified, and the caller does not have write access to the file or directory, the function fails.</p></td>
</tr>
<tr class="even">
<td><span id="FILE_SHARE_WRITE"></span><span id="file_share_write"></span>
<strong>FILE_SHARE_WRITE</strong>
0x00000002</td>
<td><p>Enables subsequent open operations on a file or device to request write access.</p>
<p>Otherwise, other processes cannot open the file or device if they request write access.</p>
<p>If this flag is not specified, but the file or device has been opened for write access or has a file mapping with write access, the function fails.</p></td>
</tr>
</tbody>
</table>

### -param dwCreationDisposition

An action to take on a file or device that exists or does not exist.
    
For devices other than files, this parameter is usually set to **OPEN\_EXISTING**.

This parameter must be one of the following values, which cannot be combined:

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Meaning</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="CREATE_ALWAYS"></span><span id="create_always"></span>
<strong>CREATE_ALWAYS</strong>
2</td>
<td><p>Creates a new file, always.</p>
<p>If the specified file exists and is writable, the function truncates the file, the function succeeds, and last-error code is set to <strong>ERROR_ALREADY_EXISTS</strong> (183).</p>
<p>If the specified file does not exist and is a valid path, a new file is created, the function succeeds, and the last-error code is set to zero.</p></td>
</tr>
<tr class="even">
<td><span id="CREATE_NEW"></span><span id="create_new"></span>
<strong>CREATE_NEW</strong>
1</td>
<td><p>Creates a new file, only if it does not already exist.</p>
<p>If the specified file exists, the function fails and the last-error code is set to <strong>ERROR_FILE_EXISTS</strong> (80).</p>
<p>If the specified file does not exist and is a valid path to a writable location, a new file is created.</p></td>
</tr>
<tr class="odd">
<td><span id="OPEN_ALWAYS"></span><span id="open_always"></span>
<strong>OPEN_ALWAYS</strong>
4</td>
<td><p>Opens a file, always.</p>
<p>If the specified file exists, the function succeeds and the last-error code is set to <strong>ERROR_ALREADY_EXISTS</strong> (183).</p>
<p>If the specified file does not exist and is a valid path to a writable location, the function creates a file and the last-error code is set to zero.</p></td>
</tr>
<tr class="even">
<td><span id="OPEN_EXISTING"></span><span id="open_existing"></span>
<strong>OPEN_EXISTING</strong>
3</td>
<td><p>Opens a file or device, only if it exists.</p>
<p>If the specified file or device does not exist, the function fails and the last-error code is set to <strong>ERROR_FILE_NOT_FOUND</strong> (2).</p></td>
</tr>
<tr class="odd">
<td><span id="TRUNCATE_EXISTING"></span><span id="truncate_existing"></span>
<strong>TRUNCATE_EXISTING</strong>
5</td>
<td><p>Opens a file and truncates it so that its size is zero bytes, only if it exists.</p>
<p>If the specified file does not exist, the function fails and the last-error code is set to <strong>ERROR_FILE_NOT_FOUND</strong> (2).</p>
<p>The calling process must open the file with the <strong>GENERIC_WRITE</strong> bit set as part of the <em>dwDesiredAccess</em> parameter.</p></td>
</tr>
</tbody>
</table>

### -param pCreateExParams

Pointer to an optional [**CREATEFILE2\_EXTENDED\_PARAMETERS**](../fileapi/ns-fileapi-createfile2_extended_parameters.md) structure.


## -returns

If the function succeeds, the return value is an open handle to the specified file, device, named pipe, or mail slot.

If the function fails, the return value is **INVALID\_HANDLE\_VALUE**. To get extended error information, call [**GetLastError**](../errhandlingapi/nf-errhandlingapi-getlasterror.md).


## -remarks

## -see-also

