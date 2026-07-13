---
UID: NS:winbase.COPYFILE2_EXTENDED_PARAMETERS_V2
tech.root: fs
title: COPYFILE2_EXTENDED_PARAMETERS_V2
ms.date: 11/02/2023
targetos: Windows
description: Contains updated, additional functionality beyond the COPYFILE2_EXTENDED_PARAMETERS structure for the CopyFile2 function
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: winbase.h
req.include-header: Windows.h
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 11 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.target-type: Windows
req.typenames: COPYFILE2_EXTENDED_PARAMETERS_V2
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winbase.h
api_name:
 - COPYFILE2_EXTENDED_PARAMETERS_V2
f1_keywords:
 - COPYFILE2_EXTENDED_PARAMETERS_V2
 - winbase/COPYFILE2_EXTENDED_PARAMETERS_V2
dev_langs:
 - c++
helpviewer_keywords:
 - COPYFILE2_EXTENDED_PARAMETERS_V2
---

## -description

Contains updated, additional functionality beyond the [COPYFILE2_EXTENDED_PARAMETERS](ns-winbase-copyfile2_extended_parameters.md) structure for the [CopyFile2](nf-winbase-copyfile2.md) function.

## -struct-fields

### -field dwSize

Contains the size of this structure, `sizeof(COPYFILE2_EXTENDED_PARAMETERS_V2)`.

### -field dwCopyFlags

Contains a combination of zero or more of these flag values.

| Value | Meaning |
| ----- | ------- |
| **COPY_FILE_FAIL_IF_EXISTS**<br/>`0x00000001` | If the destination file exists the copy operation fails immediately. If a file or directory exists with the destination name then the [CopyFile2](/windows/win32/api/winbase/nf-winbase-copyfile2) function call will fail with either `HRESULT_FROM_WIN32(ERROR_ALREADY_EXISTS)` or `HRESULT_FROM_WIN32(ERROR_FILE_EXISTS)`. If **COPY_FILE_RESUME_FROM_PAUSE** is also specified then a failure is only triggered if the destination file does not have a valid restart header. |
| **COPY_FILE_RESTARTABLE**<br/>`0x00000002` | The file is copied in a manner that can be restarted if the same source and destination filenames are used again. This is slower. |
| **COPY_FILE_OPEN_SOURCE_FOR_WRITE**<br/>`0x00000004` | The file is copied and the source file is opened for write access. |
| **COPY_FILE_ALLOW_DECRYPTED_DESTINATION**<br/>`0x00000008` | The copy will be attempted even if the destination file cannot be encrypted. |
| **COPY_FILE_COPY_SYMLINK**<br/>`0x00000800` | If the source file is a symbolic link, the destination file is also a symbolic link pointing to the same file as the source symbolic link. |
| **COPY_FILE_NO_BUFFERING**<br/>`0x00001000` | The copy is performed using unbuffered I/O, bypassing the system cache resources. This flag is recommended for very large file copies. It is not recommended to pause copies that are using this flag. |
| **COPY_FILE_REQUEST_SECURITY_PRIVILEGES**<br/>`0x00002000` | The copy is attempted, specifying `ACCESS_SYSTEM_SECURITY` for the source file and `ACCESS_SYSTEM_SECURITY \| WRITE_DAC \| WRITE_OWNER` for the destination file. If these requests are denied the access request will be reduced to the highest privilege level for which access is granted. For more information see [SACL Access Right](/windows/win32/SecAuthZ/sacl-access-right). This can be used to allow the [CopyFile2ProgressRoutine](/windows/win32/api/winbase/nc-winbase-pcopyfile2_progress_routine) callback to perform operations requiring higher privileges, such as copying the security attributes for the file. |
| **COPY_FILE_RESUME_FROM_PAUSE**<br/>`0x00004000` | The destination file is examined to see if it was copied using **COPY_FILE_RESTARTABLE**. If so the copy is resumed. If not the file will be fully copied. |
| **COPY_FILE_NO_OFFLOAD**<br/>`0x00040000` | Do not attempt to use the Windows Copy Offload mechanism. This is not generally recommended. |
| **COPY_FILE_IGNORE_EDP_BLOCK**<br/>`0x00400000` | Instead of blocking, the file should be copied and encrypted on the destination if supported by the destination file system. **Supported on Windows 10 and later.** |
| **COPY_FILE_IGNORE_SOURCE_ENCRYPTION**<br/>`0x00800000` | Ignore the source file’s encrypted state. **Supported on Windows 10 and later.** |
| **COPY_FILE_DONT_REQUEST_DEST_WRITE_DAC**<br/>`0x02000000` | Don't request WRITE_DAC for the destination file access. **Supported on Windows 10 and later.** |
| **COPY_FILE_OPEN_AND_COPY_REPARSE_POINT**<br/>`0x00200000` | Always copy the reparse point regardless of type. It's the caller’s responsibility to understand the reparse point meaning. **Supported on Windows 10, build 19041 and later.** |
| **COPY_FILE_DIRECTORY**<br/>`0x00000080` | Indicates the source file is a directory file. When provided, the source file is opened with `FILE_OPEN_FOR_BACKUP_INTENT`. The directory file will have its alternate data streams, reparse point info, and EAs copied like a normal file. **Supported in Windows 10, build 19041 and later.** |
| **COPY_FILE_SKIP_ALTERNATE_STREAMS**<br/>`0x00008000` | Do not copy alternate data streams. **Supported in Windows 10, build 19041 and later.** |
| **COPY_FILE_DISABLE_PRE_ALLOCATION**<br/>`0x04000000` | Do not preallocate the destination file size before performing the copy. **Supported in Windows 10, build 19041 and later.** |
| **COPY_FILE_ENABLE_LOW_FREE_SPACE_MODE**<br/>`0x08000000` | Enable LowFreeSpace mode. No overlapped I/Os are used. ODX and SMB offload are not attempted. **Supported in Windows 10, build 19041 and later.** |
| **COPY_FILE_REQUEST_COMPRESSED_TRAFFIC**<br/>`0x10000000` | Request the underlying transfer channel compress the data during the copy operation. The request may not be supported for all mediums, in which case it is ignored. The compression attributes and parameters (computational complexity, memory usage) are not configurable through this API, and are subject to change between different OS releases.<br/><br/>This flag was introduced in Windows 10, version 1903 and Windows Server 2022. On Windows 10, the flag is supported for files residing on SMB shares, where the negotiated SMB protocol version is SMB v3.1.1 or greater. |
| **COPY_FILE_ENABLE_SPARSE_COPY**<br/>`0x20000000` | Enable retaining the sparse state of the file during copy. **Supported in Windows 11, build 22H2 and later.** |

### -field pfCancel

If this flag is set to **TRUE** during the copy operation then the copy operation is canceled.

### -field pProgressRoutine

The optional address of a callback function of type **PCOPYFILE2_PROGRESS_ROUTINE** that is called each time another portion of the file has been copied. This parameter can be **NULL**. For more information on the progress callback function, see the [CopyFile2ProgressRoutine](nc-winbase-pcopyfile2_progress_routine.md) callback function. If both *pProgressRoutineOld* and *pProgressRoutine* are provided, *pProgressRoutineOld* takes precedence.

### -field pvCallbackContext

A pointer to application-specific context information to be passed to the [CopyFile2ProgressRoutine](nc-winbase-pcopyfile2_progress_routine.md).

### -field dwCopyFlagsV2

Contains a combination of zero or more of these flag values.

| Value | Meaning |
| ----- | ------- |
| **COPY_FILE2_V2_DONT_COPY_JUNCTIONS**<br/>`0x00000001` | Disable copying junctions. |

### -field ioDesiredSize

Optional. The requested size (in bytes) for each I/O operation (i.e. one read/write cycle while copying the file). This may be reduced if insufficient memory is available. If zero, the default size is used. This may be ignored if *ioDesiredRate* is also provided

### -field ioDesiredRate

Optional. The requested average I/O rate, in kilobytes per second. If zero, copies are performed as fast as possible.

### -field reserved[8]

*pProgressRoutineOld*. Optional. The address of an old-style callback function of type [LPPROGRESS_ROUTINE](nc-winbase-lpprogress_routine.md) that is called each time another portion of the file has been copied. This parameter can be **NULL**. For more information, on the progress callback function, see [LPPROGRESS_ROUTINE callback](nc-winbase-lpprogress_routine.md). If both *pProgressRoutineOld* and *pProgressRoutine* are provided, *pProgressRoutineOld* takes precedence.

## -remarks

To compile an application that uses this structure, define the **_WIN32_WINNT** macro as **_WIN32_WINNT_WIN8** or later. For more information, see [Using the Windows Headers](/windows/win32/winprog/using-the-windows-headers).

## -see-also

[CopyFile2](nf-winbase-copyfile2.md)

[COPYFILE2_EXTENDED_PARAMETERS](ns-winbase-copyfile2_extended_parameters.md)

[CopyFile2ProgressRoutine](nc-winbase-pcopyfile2_progress_routine.md)

[File Management Structures](/windows/win32/fileio/file-management-structures)

[LPPROGRESS_ROUTINE](nc-winbase-lpprogress_routine.md)

[Using the Windows Headers](/windows/win32/winprog/using-the-windows-headers)
