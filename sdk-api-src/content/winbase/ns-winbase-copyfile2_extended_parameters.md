---
UID: NS:winbase.COPYFILE2_EXTENDED_PARAMETERS
title: COPYFILE2_EXTENDED_PARAMETERS (winbase.h)
description: Contains extended parameters for the CopyFile2 function.
helpviewer_keywords: ["COPYFILE2_EXTENDED_PARAMETERS","COPYFILE2_EXTENDED_PARAMETERS structure [Files]","COPY_FILE_ALLOW_DECRYPTED_DESTINATION","COPY_FILE_COPY_SYMLINK","COPY_FILE_FAIL_IF_EXISTS","COPY_FILE_NO_BUFFERING","COPY_FILE_NO_OFFLOAD","COPY_FILE_OPEN_SOURCE_FOR_WRITE","COPY_FILE_REQUEST_SECURITY_PRIVILEGES","COPY_FILE_RESTARTABLE","COPY_FILE_RESUME_FROM_PAUSE","fs.copyfile2_extended_parameters","winbase/COPYFILE2_EXTENDED_PARAMETERS"]
old-location: fs\copyfile2_extended_parameters.htm
tech.root: fs
ms.assetid: a8da62e5-bc49-4aff-afaa-e774393b7120
ms.date: 12/05/2018
ms.keywords: COPYFILE2_EXTENDED_PARAMETERS, COPYFILE2_EXTENDED_PARAMETERS structure [Files], COPY_FILE_ALLOW_DECRYPTED_DESTINATION, COPY_FILE_COPY_SYMLINK, COPY_FILE_FAIL_IF_EXISTS, COPY_FILE_NO_BUFFERING, COPY_FILE_NO_OFFLOAD, COPY_FILE_OPEN_SOURCE_FOR_WRITE, COPY_FILE_REQUEST_SECURITY_PRIVILEGES, COPY_FILE_RESTARTABLE, COPY_FILE_RESUME_FROM_PAUSE, fs.copyfile2_extended_parameters, winbase/COPYFILE2_EXTENDED_PARAMETERS
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: COPYFILE2_EXTENDED_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - COPYFILE2_EXTENDED_PARAMETERS
 - winbase/COPYFILE2_EXTENDED_PARAMETERS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - COPYFILE2_EXTENDED_PARAMETERS
---

# COPYFILE2_EXTENDED_PARAMETERS structure

## -description

Contains extended parameters for the [CopyFile2 function](nf-winbase-copyfile2.md).

## -struct-fields

### -field dwSize

Contains the size of this structure, `sizeof(COPYFILE2_EXTENDED_PARAMETERS)`.

### -field dwCopyFlags

Contains a combination of zero or more of these flag values.

| Value | Meaning |
|---|---|
| **COPY_FILE_ALLOW_DECRYPTED_DESTINATION**<br>0x00000008 | The copy will be attempted even if the destination file cannot be encrypted. |
| **COPY_FILE_COPY_SYMLINK**<br>0x00000800 | If the source file is a symbolic link, the destination file is also a symbolic link pointing to the same file as the source symbolic link. |
| **COPY_FILE_FAIL_IF_EXISTS**<br>0x00000001 | If the destination file exists the copy operation fails immediately. If a file or directory exists with the destination name then the [CopyFile2](nf-winbase-copyfile2.md) function call will fail with either `HRESULT_FROM_WIN32(ERROR_ALREADY_EXISTS)` or `HRESULT_FROM_WIN32(ERROR_FILE_EXISTS)`. If **COPY_FILE_RESUME_FROM_PAUSE** is also specified then a failure is only triggered if the destination file does not have a valid restart header. |
| **COPY_FILE_NO_BUFFERING**<br>0x00001000 | The copy is performed using unbuffered I/O, bypassing the system cache resources. This flag is recommended for very large file copies. It is not recommended to pause copies that are using this flag. |
| **COPY_FILE_NO_OFFLOAD**<br>0x00040000 | Do not attempt to use the Windows Copy Offload mechanism. This is not generally recommended. |
| **COPY_FILE_OPEN_SOURCE_FOR_WRITE**<br>0x00000004 | The file is copied and the source file is opened for write access. |
| **COPY_FILE_RESTARTABLE**<br>0x00000002 | The file is copied in a manner that can be restarted if the same source and destination filenames are used again. This is slower. |
| **COPY_FILE_REQUEST_SECURITY_PRIVILEGES**<br>0x00002000 | The copy is attempted, specifying `ACCESS_SYSTEM_SECURITY` for the source file and `ACCESS_SYSTEM_SECURITY \| WRITE_DAC \| WRITE_OWNER` for the destination file. If these requests are denied the access request will be reduced to the highest privilege level for which access is granted. For more information see [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right). This can be used to allow the [CopyFile2ProgressRoutine callback](/windows/desktop/api/winbase/nc-winbase-pcopyfile2_progress_routine) to perform operations requiring higher privileges, such as copying the security attributes for the file. |
| **COPY_FILE_RESUME_FROM_PAUSE**<br>0x00004000 | The destination file is examined to see if it was copied using **COPY_FILE_RESTARTABLE**. If so the copy is resumed. If not the file will be fully copied. |
| **COPY_FILE_REQUEST_COMPRESSED_TRAFFIC**<br>0x10000000 | Request the underlying transfer channel compress the data during the copy operation. The request may not be supported for all mediums, in which case it is ignored. The compression attributes and parameters (computational complexity, memory usage) are not configurable through this API, and are subject to change between different OS releases.
This flag was introduced in Windows 10, version 1903 and Windows Server 2022. On Windows 10, the flag is supported for files residing on SMB shares, where the negotiated SMB protocol version is SMB v3.1.1 or greater. |

### -field pfCancel

If this flag is set to <b>TRUE</b> during the copy operation then the copy operation is 
      canceled.

### -field pProgressRoutine

The optional address of a callback function of type <b>PCOPYFILE2_PROGRESS_ROUTINE</b> that is 
      called each time another portion of the file has been copied. This parameter can be 
      <b>NULL</b>. For more information on the progress callback function, see the 
      <a href="/windows/desktop/api/winbase/nc-winbase-pcopyfile2_progress_routine">CopyFile2ProgressRoutine</a> callback function.

### -field pvCallbackContext

A pointer to application-specific context information to be passed to the 
      <a href="/windows/desktop/api/winbase/nc-winbase-pcopyfile2_progress_routine">CopyFile2ProgressRoutine</a>.

## -remarks

To compile an application that uses this structure, define the <b>_WIN32_WINNT</b> 
    macro as <b>_WIN32_WINNT_WIN8</b> or later. For more information, see 
    <a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-copyfile2">CopyFile2</a>



<a href="/windows/desktop/api/winbase/nc-winbase-pcopyfile2_progress_routine">CopyFile2ProgressRoutine</a>



<a href="/windows/desktop/FileIO/file-management-structures">File Management Structures</a>