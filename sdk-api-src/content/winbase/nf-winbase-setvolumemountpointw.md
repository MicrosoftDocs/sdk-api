---
UID: NF:winbase.SetVolumeMountPointW
title: SetVolumeMountPointW function (winbase.h)
description: Associates a volume with a drive letter or a directory on another volume. (Unicode)
helpviewer_keywords: ["SetVolumeMountPoint", "SetVolumeMountPoint function [Files]", "SetVolumeMountPointW", "_win32_setvolumemountpoint", "base.setvolumemountpoint", "fs.setvolumemountpoint", "winbase/SetVolumeMountPoint", "winbase/SetVolumeMountPointW"]
old-location: fs\setvolumemountpoint.htm
tech.root: fs
ms.assetid: 1535fe64-221a-4756-a9ba-81bbe7596598
ms.date: 12/05/2018
ms.keywords: SetVolumeMountPoint, SetVolumeMountPoint function [Files], SetVolumeMountPointA, SetVolumeMountPointW, _win32_setvolumemountpoint, base.setvolumemountpoint, fs.setvolumemountpoint, winbase/SetVolumeMountPoint, winbase/SetVolumeMountPointA, winbase/SetVolumeMountPointW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetVolumeMountPointW (Unicode) and SetVolumeMountPointA (ANSI)
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
 - SetVolumeMountPointW
 - winbase/SetVolumeMountPointW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - SetVolumeMountPoint
 - SetVolumeMountPointA
 - SetVolumeMountPointW
---

# SetVolumeMountPointW function


## -description

Associates a volume with a drive letter or a directory on another volume.

## -parameters

### -param lpszVolumeMountPoint [in]

The user-mode path to be associated with the volume. This may be a drive letter (for example, "X:\\") or a directory 
      on another volume (for example, "Y:\\MountX\\"). The string must end with a trailing backslash ('\\').

### -param lpszVolumeName [in]

A volume <b>GUID</b> path for the volume. This string must be of the form 
      "\\\\?\\Volume{<i>GUID</i>}\\" where <i>GUID</i> is a <b>GUID</b> that identifies 
      the volume. The "\\\\?\\" turns off path parsing and is ignored as part of the path, as discussed in 
      <a href="/windows/desktop/FileIO/naming-a-volume">Naming a Volume</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the <i>lpszVolumeMountPoint</i> parameter contains a path to a mounted folder, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_DIR_NOT_EMPTY</b>, even if the directory is empty.

## -remarks

When this function is used to associate a volume with a directory on another volume, the associated directory is called a <i>mounted folder</i>.

It is an error to associate a volume with a directory that has any files or subdirectories in it. This 
    error occurs for system and hidden directories as well as other directories, and it occurs for system and hidden 
    files.

When mounted folders are created on a volume on a clustered disk, they may be deleted unexpectedly under certain 
    circumstances. For information on how to create and configure mounted folders to ensure that this does not happen, 
    see <a href="/previous-versions/windows/it-pro/windows-server-2003/cc757627(v=ws.10)">Cluster Disk and Drive Connection Problems</a>.

IIn Windows 8 and Windows Server 2012, this function is supported by the following technologies.

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
No

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
Cluster Shared Volume File System (CsvFS)

</td>
<td>
No

</td>
</tr>
<tr>
<td>
Resilient File System (ReFS)

</td>
<td>
No

</td>
</tr>
</table>
 

SMB does not support volume management functions. For CsvFS a new mount point will not be replicated to the other nodes on the cluster.


#### Examples

For an example, see 
     <a href="/windows/desktop/FileIO/mounting-a-volume-at-a-mount-point">Creating a Mounted Folder</a>.

<div class="code"></div>




> [!NOTE]
> The winbase.h header defines SetVolumeMountPoint as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-deletevolumemountpointw">DeleteVolumeMountPoint</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumenameforvolumemountpointw">GetVolumeNameForVolumeMountPoint</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumepathnamew">GetVolumePathName</a>



<a href="/windows/desktop/FileIO/volume-mount-points">Mounted Folders</a>



<a href="/windows/desktop/FileIO/volume-management-functions">Volume Management Functions</a>
