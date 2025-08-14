---
UID: NF:fileapi.GetVolumePathNameW
title: GetVolumePathNameW function (fileapi.h)
description: Retrieves the volume mount point where the specified path is mounted. (GetVolumePathNameW)
helpviewer_keywords: ["GetVolumePathName","GetVolumePathName function [Files]","GetVolumePathNameA","GetVolumePathNameW","_win32_getvolumepathname","base.getvolumepathname","fileapi/GetVolumePathName","fileapi/GetVolumePathNameA","fileapi/GetVolumePathNameW","fs.getvolumepathname","winbase/GetVolumePathName","winbase/GetVolumePathNameA","winbase/GetVolumePathNameW"]
old-location: fs\getvolumepathname.htm
tech.root: fs
ms.assetid: fa34786c-af82-4b59-bf36-e9a95a2f913e
ms.date: 12/05/2018
ms.keywords: GetVolumePathName, GetVolumePathName function [Files], GetVolumePathNameA, GetVolumePathNameW, _win32_getvolumepathname, base.getvolumepathname, fileapi/GetVolumePathName, fileapi/GetVolumePathNameA, fileapi/GetVolumePathNameW, fs.getvolumepathname, winbase/GetVolumePathName, winbase/GetVolumePathNameA, winbase/GetVolumePathNameW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi: GetVolumePathNameW (Unicode) and GetVolumePathNameA (ANSI)
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
 - GetVolumePathNameW
 - fileapi/GetVolumePathNameW
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
 - API-Ms-Win-Core-File-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - GetVolumePathName
 - GetVolumePathNameA
 - GetVolumePathNameW
---

# GetVolumePathNameW function

## -description

Retrieves the volume mount point where the specified path is mounted.

## -parameters

### -param lpszFileName [in]

A pointer to the input path string. Both absolute and relative file and directory names, for example, "..", are acceptable in this path.

If you specify a relative directory or file name without a volume qualifier, **GetVolumePathName** returns the drive letter of the boot volume.

If this parameter is an empty string, "", the function fails but the last error is set to **ERROR_SUCCESS**.

### -param lpszVolumePathName [out]

A pointer to a string that receives the volume mount point for the input path.

### -param cchBufferLength [in]

The length of the output buffer, in **TCHARs**.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## -remarks

If a specified path is passed, **GetVolumePathName** returns the path to the volume mount point, which means that it returns the root of the volume where the end point of the specified path is located.

For example, assume that you have volume D mounted at `C:\Mnt\Ddrive` and volume E mounted at `C:\Mnt\Ddrive\Mnt\Edrive`. Also assume that you have a file with the path `E:\Dir\Subdir\MyFile`. If you pass `C:\Mnt\Ddrive\Mnt\Edrive\Dir\Subdir\MyFile` to **GetVolumePathName**, it returns the path `C:\Mnt\Ddrive\Mnt\Edrive\`.

If either a relative directory or a file is passed without a volume qualifier, the function returns the drive letter of the boot volume. The drive letter of the boot volume is also returned if an invalid file or directory name is specified without a valid volume qualifier. If a valid volume specifier is given, and the volume exists, but an invalid file or directory name is specified, the function will succeed and that volume name will be returned. For examples, see the Examples section of this topic.

You must specify a valid Win32 namespace path. If you specify an NT namespace path, for example, `\DosDevices\H:` or `\Device\HardDiskVolume6`, the function returns the drive letter of the boot volume, not the drive letter of that NT namespace path.

For more information about path names and namespaces, see [Naming Files, Paths, and Namespaces](/windows/win32/FileIO/naming-a-file).

You can specify both local and remote paths. If you specify a local path, **GetVolumePathName** returns a full path whose prefix is the longest prefix that represents a volume.

If a network share is specified, **GetVolumePathName** returns the shortest path for which [GetDriveType](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea) returns **DRIVE_REMOTE**, which means that the path is validated as a remote drive that exists, which the current user can access.

There are certain special cases that do not return a trailing backslash. These occur when the output buffer length is one character too short. For example, if _lpszFileName_ is `C:` and _lpszVolumePathName_ is 4 characters long, the value returned is `C:\`; however, if _lpszVolumePathName_ is 3 characters long, the value returned is `C:`. A safer but slower way to set the size of the return buffer is to call the [GetFullPathName](/windows/win32/api/fileapi/nf-fileapi-getfullpathnamea) function, and then make sure that the buffer size is at least the same size as the full path that **GetFullPathName** returns. If the output buffer is more than one character too short, the function will fail and return an error.

In Windows 8 and Windows Server 2012, this function is supported by the following technologies.

Technology | Supported
-----------|----------
Server Message Block (SMB) 3.0 protocol|No
SMB 3.0 Transparent Failover (TFO)|No
SMB 3.0 with Scale-out File Shares (SO)|No
Cluster Shared Volume File System (CsvFS)|Yes
Resilient File System (ReFS)|Yes

SMB does not support volume management functions.

### Trailing Path Elements

Trailing path elements that are invalid are ignored. For remote paths, the entire path (not just trailing elements) is considered invalid if one of the following conditions is true:

* The path is not formed correctly.
* The path does not exist.
* The current user does not have access to the path.

### Junction Points and Mounted Folders

If the specified path traverses a junction point, **GetVolumePathName** returns the volume to which the   junction point refers. For example, if `W:\Adir` is a junction point that points to `C:\Adir`, then **GetVolumePathName** invoked on `W:\Adir\Afile` returns `C:\`. If the specified path traverses multiple junction points, the entire chain is followed, and **GetVolumePathName** returns the volume to which the   last junction point in the chain refers.

If a remote path to a mounted folder or junction point is specified, the path is parsed as a remote path, and   the mounted folder or junction point are ignored. For example if `C:\Dir_C` is linked to `D:\Dir_D` and `C:` is mapped to `X:` on a remote computer, calling  **GetVolumePathName** and specifying `X:\Dir_C` on the remote computer returns `X:\`.

#### Examples

For the following set of examples, U: is mapped to the remote computer  `\\_YourComputer_\C$`, and Q is a local drive.

Specified path                     | Function returns
-----------------------------------|-----------------
`\\_YourComputer_\C$\Windows`      | `\\_YourComputer_\C$\`
`\\?\UNC\_YourComputer_\C$\Windows`| `\\?\UNC\_YourComputer_\C$\`
`Q:\Windows`                       | `Q:\`
`\\?\Q:\Windows`                   | `\\?\Q:\`
`\\.\Q:\Windows`                   | `\\.\Q:\`
`\\?\UNC\W:\Windows`               | **FALSE** with error 123 because a specified remote path was not valid; W$ share does not exist or no user access granted.
`C:\COM2` (which exists)           | `\\.\COM2\`
`C:\COM3` (non-existent)           | **FALSE** with error 123 because a non-existent COM device was specified.

For the following set of examples, the paths contain invalid trailing path elements.

Specified path                                                | Function returns
--------------------------------------------------------------|-----------------
`G:\invalid` (invalid path)                                   | `G:\`
`\\.\I:\aaa\invalid` (invalid path)                           | `\\.\I:\`
`\\_YourComputer_\C$\invalid` (invalid trailing path element) | `\\_YourComputer_\C$\`

## -see-also

* [DeleteVolumeMountPoint](/windows/win32/api/fileapi/nf-fileapi-deletevolumemountpointw)
* [GetFullPathName](/windows/win32/api/fileapi/nf-fileapi-getfullpathnamea)
* [GetVolumeNameForVolumeMountPoint](/windows/win32/api/fileapi/nf-fileapi-getvolumenameforvolumemountpointw)
* [SetVolumeMountPoint](/windows/win32/api/winbase/nf-winbase-setvolumemountpointa)
* [Volume Management Functions](/windows/win32/FileIO/volume-management-functions)
* [Volume Mount Points](/windows/win32/FileIO/volume-mount-points)
