---
UID: NF:fileapi.FindNextVolumeW
title: FindNextVolumeW function (fileapi.h)
description: Continues a volume search started by a call to the FindFirstVolume function. (FindNextVolumeW)
helpviewer_keywords: ["FindNextVolume","FindNextVolume function [Files]","FindNextVolumeA","FindNextVolumeW","_win32_findnextvolume","base.findnextvolume","fileapi/FindNextVolume","fileapi/FindNextVolumeA","fileapi/FindNextVolumeW","fs.findnextvolume","winbase/FindNextVolume","winbase/FindNextVolumeA","winbase/FindNextVolumeW"]
old-location: fs\findnextvolume.htm
tech.root: fs
ms.assetid: 6ab4467a-f84a-403e-9327-b523ceead19f
ms.date: 12/05/2018
ms.keywords: FindNextVolume, FindNextVolume function [Files], FindNextVolumeA, FindNextVolumeW, _win32_findnextvolume, base.findnextvolume, fileapi/FindNextVolume, fileapi/FindNextVolumeA, fileapi/FindNextVolumeW, fs.findnextvolume, winbase/FindNextVolume, winbase/FindNextVolumeA, winbase/FindNextVolumeW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindNextVolumeW (Unicode) and FindNextVolumeA (ANSI)
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
 - FindNextVolumeW
 - fileapi/FindNextVolumeW
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
 - FindNextVolume
 - FindNextVolumeA
 - FindNextVolumeW
---

# FindNextVolumeW function


## -description

Continues a volume search started by a call to the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstvolumew">FindFirstVolume</a> function. <b>FindNextVolume</b> finds one volume per call.

## -parameters

### -param hFindVolume [in]

The volume search handle returned by a previous call to the 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstvolumew">FindFirstVolume</a> function.

### -param lpszVolumeName [out]

A pointer to a string that receives the volume <b>GUID</b> path that is found.

### -param cchBufferLength [in]

The length of the buffer that receives the volume <b>GUID</b> path, in 
      <b>TCHARs</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If no matching files can be found, the 
       <b>GetLastError</b> function returns the 
       <b>ERROR_NO_MORE_FILES</b> error code. In that case, close the search with the 
       <a href="/windows/desktop/api/fileapi/nf-fileapi-findvolumeclose">FindVolumeClose</a> function.

## -remarks

After the search handle is established by calling 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstvolumew">FindFirstVolume</a>, you can use the 
    <b>FindNextVolume</b> function to search for other volumes.

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

<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstvolumew">FindFirstVolume</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findvolumeclose">FindVolumeClose</a>



<a href="/windows/desktop/FileIO/volume-mount-points">Mounted Folders</a>



<a href="/windows/desktop/FileIO/volume-management-functions">Volume Management Functions</a>
