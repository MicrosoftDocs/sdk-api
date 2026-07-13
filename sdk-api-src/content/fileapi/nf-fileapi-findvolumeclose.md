---
UID: NF:fileapi.FindVolumeClose
title: FindVolumeClose function (fileapi.h)
description: Closes the specified volume search handle.
helpviewer_keywords: ["FindVolumeClose","FindVolumeClose function [Files]","_win32_findvolumeclose","base.findvolumeclose","fileapi/FindVolumeClose","fs.findvolumeclose","winbase/FindVolumeClose"]
old-location: fs\findvolumeclose.htm
tech.root: fs
ms.assetid: 091a2f0c-df38-4fef-a926-3507545bb58d
ms.date: 12/05/2018
ms.keywords: FindVolumeClose, FindVolumeClose function [Files], _win32_findvolumeclose, base.findvolumeclose, fileapi/FindVolumeClose, fs.findvolumeclose, winbase/FindVolumeClose
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - FindVolumeClose
 - fileapi/FindVolumeClose
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
api_name:
 - FindVolumeClose
---

# FindVolumeClose function


## -description

Closes the specified volume search handle. The <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstvolumew">FindFirstVolume</a> and 
<a href="/windows/desktop/api/fileapi/nf-fileapi-findnextvolumew">FindNextVolume</a> functions use this search handle to locate volumes.

## -parameters

### -param hFindVolume [in]

The volume search handle to be closed. This handle must have been previously opened by the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstvolumew">FindFirstVolume</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

After the 
<b>FindVolumeClose</b> function is called, the handle <i>hFindVolume</i> cannot be used in subsequent calls to either 
<a href="/windows/desktop/api/fileapi/nf-fileapi-findnextvolumew">FindNextVolume</a> or 
<b>FindVolumeClose</b>.

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



<a href="/windows/desktop/api/fileapi/nf-fileapi-findnextvolumew">FindNextVolume</a>



<a href="/windows/desktop/FileIO/volume-mount-points">Mounted Folders</a>



<a href="/windows/desktop/FileIO/volume-management-functions">Volume Management Functions</a>