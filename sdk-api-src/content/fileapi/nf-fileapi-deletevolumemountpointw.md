---
UID: NF:fileapi.DeleteVolumeMountPointW
title: DeleteVolumeMountPointW function (fileapi.h)
description: Deletes a drive letter or mounted folder. (DeleteVolumeMountPointW)
helpviewer_keywords: ["DeleteVolumeMountPoint","DeleteVolumeMountPoint function [Files]","DeleteVolumeMountPointA","DeleteVolumeMountPointW","_win32_deletevolumemountpoint","base.deletevolumemountpoint","fileapi/DeleteVolumeMountPoint","fileapi/DeleteVolumeMountPointA","fileapi/DeleteVolumeMountPointW","fs.deletevolumemountpoint","winbase/DeleteVolumeMountPoint","winbase/DeleteVolumeMountPointA","winbase/DeleteVolumeMountPointW"]
old-location: fs\deletevolumemountpoint.htm
tech.root: fs
ms.assetid: b1a0a273-fa7f-4794-8b50-c74f00b0228d
ms.date: 12/05/2018
ms.keywords: DeleteVolumeMountPoint, DeleteVolumeMountPoint function [Files], DeleteVolumeMountPointA, DeleteVolumeMountPointW, _win32_deletevolumemountpoint, base.deletevolumemountpoint, fileapi/DeleteVolumeMountPoint, fileapi/DeleteVolumeMountPointA, fileapi/DeleteVolumeMountPointW, fs.deletevolumemountpoint, winbase/DeleteVolumeMountPoint, winbase/DeleteVolumeMountPointA, winbase/DeleteVolumeMountPointW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DeleteVolumeMountPointW (Unicode) and DeleteVolumeMountPointA (ANSI)
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
 - DeleteVolumeMountPointW
 - fileapi/DeleteVolumeMountPointW
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
 - DeleteVolumeMountPoint
 - DeleteVolumeMountPointA
 - DeleteVolumeMountPointW
---

# DeleteVolumeMountPointW function


## -description

Deletes a drive letter or mounted folder.

## -parameters

### -param lpszVolumeMountPoint [in]

The drive letter or mounted folder to be deleted. A trailing backslash is required, for example, 
      "X:\" or "Y:\MountX\".

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Deleting a mounted folder does not cause the underlying directory to be deleted.

If the <i>lpszVolumeMountPoint</i> parameter is a directory that is not a mounted folder, 
    the function does nothing. The directory is not deleted.

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
 

SMB does not support volume management functions. For CsvFs, a new mount point will not be replicated to the other nodes on the cluster.



#### Examples

For an example, see 
     <a href="/windows/desktop/FileIO/unmounting-a-volume-at-a-mount-point">Unmounting a Volume at a Mount Point</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumenameforvolumemountpointw">GetVolumeNameForVolumeMountPoint</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumepathnamew">GetVolumePathName</a>



<a href="/windows/desktop/FileIO/volume-mount-points">Mounted Folders</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setvolumemountpointa">SetVolumeMountPoint</a>



<a href="/windows/desktop/FileIO/volume-management-functions">Volume Management Functions</a>
