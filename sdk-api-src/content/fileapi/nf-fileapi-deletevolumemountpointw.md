---
UID: NF:fileapi.DeleteVolumeMountPointW
title: DeleteVolumeMountPointW function (fileapi.h)
author: windows-sdk-content
description: Deletes a drive letter or mounted folder.
old-location: fs\deletevolumemountpoint.htm
tech.root: FileIO
ms.assetid: b1a0a273-fa7f-4794-8b50-c74f00b0228d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeleteVolumeMountPoint, DeleteVolumeMountPoint function [Files], DeleteVolumeMountPointA, DeleteVolumeMountPointW, _win32_deletevolumemountpoint, base.deletevolumemountpoint, fileapi/DeleteVolumeMountPoint, fileapi/DeleteVolumeMountPointA, fileapi/DeleteVolumeMountPointW, fs.deletevolumemountpoint, winbase/DeleteVolumeMountPoint, winbase/DeleteVolumeMountPointA, winbase/DeleteVolumeMountPointW
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




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
     <a href="https://msdn.microsoft.com/33049110-acf8-4db5-a9c4-bd4a884c8590">Unmounting a Volume at a Mount Point</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3f749042-bdc9-4087-bb8a-d833713472eb">GetVolumeNameForVolumeMountPoint</a>



<a href="https://msdn.microsoft.com/fa34786c-af82-4b59-bf36-e9a95a2f913e">GetVolumePathName</a>



<a href="https://msdn.microsoft.com/6de526cd-5537-4411-b43f-3c0bdac70d64">Mounted Folders</a>



<a href="https://msdn.microsoft.com/1535fe64-221a-4756-a9ba-81bbe7596598">SetVolumeMountPoint</a>



<a href="https://msdn.microsoft.com/dc985126-970c-49f2-877f-3759125e43b6">Volume Management Functions</a>
 

 

