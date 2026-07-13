---
UID: NF:fileapi.FindFirstVolumeW
title: FindFirstVolumeW function (fileapi.h)
description: Retrieves the name of a volume on a computer. (FindFirstVolumeW)
helpviewer_keywords: ["FindFirstVolume","FindFirstVolume function [Files]","FindFirstVolumeA","FindFirstVolumeW","_win32_findfirstvolume","base.findfirstvolume","fileapi/FindFirstVolume","fileapi/FindFirstVolumeA","fileapi/FindFirstVolumeW","fs.findfirstvolume","winbase/FindFirstVolume","winbase/FindFirstVolumeA","winbase/FindFirstVolumeW"]
old-location: fs\findfirstvolume.htm
tech.root: fs
ms.assetid: 3eaf9903-ae20-47e7-b32c-943bf60e7bbd
ms.date: 12/05/2018
ms.keywords: FindFirstVolume, FindFirstVolume function [Files], FindFirstVolumeA, FindFirstVolumeW, _win32_findfirstvolume, base.findfirstvolume, fileapi/FindFirstVolume, fileapi/FindFirstVolumeA, fileapi/FindFirstVolumeW, fs.findfirstvolume, winbase/FindFirstVolume, winbase/FindFirstVolumeA, winbase/FindFirstVolumeW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindFirstVolumeW (Unicode) and FindFirstVolumeA (ANSI)
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
 - FindFirstVolumeW
 - fileapi/FindFirstVolumeW
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
 - FindFirstVolume
 - FindFirstVolumeA
 - FindFirstVolumeW
---

# FindFirstVolumeW function


## -description

Retrieves the name of a volume on a computer. <b>FindFirstVolume</b> is used to begin scanning the volumes of a computer.

## -parameters

### -param lpszVolumeName [out]

A pointer to a buffer that receives a null-terminated string that specifies a volume 
      <b>GUID</b> path for the first volume that is found.

### -param cchBufferLength [in]

The length of the buffer to receive the volume <b>GUID</b> path, in 
      <b>TCHARs</b>.

## -returns

If the function succeeds, the return value is a search handle used in a subsequent call to the 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextvolumew">FindNextVolume</a> and 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-findvolumeclose">FindVolumeClose</a> functions.

If the function fails to find any volumes, the return value is the 
       <b>INVALID_HANDLE_VALUE</b> error code. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>FindFirstVolume</b> function opens a volume search handle and returns 
    information about the first volume found on a computer. After the search handle is established, you can use the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findnextvolumew">FindNextVolume</a> function to search for other volumes. When 
    the search handle is no longer needed, close it by using the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findvolumeclose">FindVolumeClose</a> function.

You should not assume any correlation between the order of the volumes that are returned by these functions 
    and the order of the volumes that are on the computer. In particular, do not assume any correlation between volume 
    order and drive letters as assigned by the BIOS (if any) or the Disk Administrator.

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
Yes

</td>
</tr>
</table>
 

SMB does not support volume management functions.


#### Examples

For an example, see 
     <a href="/windows/desktop/FileIO/displaying-volume-paths">Displaying Volume Paths</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-findnextvolumew">FindNextVolume</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findvolumeclose">FindVolumeClose</a>



<a href="/windows/desktop/FileIO/volume-mount-points">Mounted Folders</a>



<a href="/windows/desktop/FileIO/volume-management-functions">Volume Management Functions</a>
