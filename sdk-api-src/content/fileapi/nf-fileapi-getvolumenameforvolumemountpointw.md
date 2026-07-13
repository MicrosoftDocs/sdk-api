---
UID: NF:fileapi.GetVolumeNameForVolumeMountPointW
title: GetVolumeNameForVolumeMountPointW function (fileapi.h)
description: Retrieves a volume GUID path for the volume that is associated with the specified volume mount point ( drive letter, volume GUID path, or mounted folder). (GetVolumeNameForVolumeMountPointW)
helpviewer_keywords: ["GetVolumeNameForVolumeMountPoint","GetVolumeNameForVolumeMountPoint function [Files]","GetVolumeNameForVolumeMountPointA","GetVolumeNameForVolumeMountPointW","_win32_getvolumenameforvolumemountpoint","base.getvolumenameforvolumemountpoint","fileapi/GetVolumeNameForVolumeMountPoint","fileapi/GetVolumeNameForVolumeMountPointA","fileapi/GetVolumeNameForVolumeMountPointW","fs.getvolumenameforvolumemountpoint","winbase/GetVolumeNameForVolumeMountPoint","winbase/GetVolumeNameForVolumeMountPointA","winbase/GetVolumeNameForVolumeMountPointW"]
old-location: fs\getvolumenameforvolumemountpoint.htm
tech.root: fs
ms.assetid: 3f749042-bdc9-4087-bb8a-d833713472eb
ms.date: 12/05/2018
ms.keywords: GetVolumeNameForVolumeMountPoint, GetVolumeNameForVolumeMountPoint function [Files], GetVolumeNameForVolumeMountPointA, GetVolumeNameForVolumeMountPointW, _win32_getvolumenameforvolumemountpoint, base.getvolumenameforvolumemountpoint, fileapi/GetVolumeNameForVolumeMountPoint, fileapi/GetVolumeNameForVolumeMountPointA, fileapi/GetVolumeNameForVolumeMountPointW, fs.getvolumenameforvolumemountpoint, winbase/GetVolumeNameForVolumeMountPoint, winbase/GetVolumeNameForVolumeMountPointA, winbase/GetVolumeNameForVolumeMountPointW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetVolumeNameForVolumeMountPointW (Unicode) and GetVolumeNameForVolumeMountPointA (ANSI)
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
 - GetVolumeNameForVolumeMountPointW
 - fileapi/GetVolumeNameForVolumeMountPointW
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
 - API-MS-Win-Core-File-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-1.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-Ms-Win-Core-File-Ansi-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - GetVolumeNameForVolumeMountPoint
 - GetVolumeNameForVolumeMountPointA
 - GetVolumeNameForVolumeMountPointW
---

# GetVolumeNameForVolumeMountPointW function


## -description

Retrieves a volume <b>GUID</b> path for the volume that is associated with the specified volume mount point (
    drive letter, volume <b>GUID</b> path, or mounted folder).

## -parameters

### -param lpszVolumeMountPoint [in]

A pointer to a string that contains the path of a mounted folder (for example, "Y:\MountX\\") or a drive letter (for example, "X:\\"). The string must end with a trailing backslash ('\\').

### -param lpszVolumeName [out]

A pointer to a string that receives the volume <b>GUID</b> path. This path is of the form "\\\\?\Volume{<i>GUID</i>}\\" where <i>GUID</i> is a <b>GUID</b> that identifies the volume. If there is more than one volume <b>GUID</b> path for the volume, only the first one in the mount manager's cache is returned.

### -param cchBufferLength [in]

The length of the output buffer, in <b>TCHARs</b>. A reasonable size for the buffer to accommodate the largest possible volume <b>GUID</b> path is 50 characters.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Use 
<b>GetVolumeNameForVolumeMountPoint</b> to obtain a volume <b>GUID</b> path for use with functions such as <a href="/windows/desktop/api/winbase/nf-winbase-setvolumemountpointa">SetVolumeMountPoint</a> and <a href="/windows/desktop/api/winbase/nf-winbase-findfirstvolumemountpointa">FindFirstVolumeMountPoint</a> that require a volume <b>GUID</b> path as an input parameter. For more information about volume <b>GUID</b> paths, see 
<a href="/windows/desktop/FileIO/naming-a-volume">Naming A Volume</a>.

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
Yes

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
 

SMB does not support volume management functions.

Mount points aren't supported by ReFS volumes.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-deletevolumemountpointw">DeleteVolumeMountPoint</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumepathnamew">GetVolumePathName</a>



<a href="/windows/desktop/FileIO/volume-mount-points">Mounted Folders</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setvolumemountpointa">SetVolumeMountPoint</a>



<a href="/windows/desktop/FileIO/volume-management-functions">Volume Management Functions</a>
