---
UID: NF:fileapi.GetVolumePathNamesForVolumeNameW
title: GetVolumePathNamesForVolumeNameW function (fileapi.h)
description: Retrieves a list of drive letters and mounted folder paths for the specified volume. (GetVolumePathNamesForVolumeNameW)
helpviewer_keywords: ["GetVolumePathNamesForVolumeName","GetVolumePathNamesForVolumeName function [Files]","GetVolumePathNamesForVolumeNameA","GetVolumePathNamesForVolumeNameW","_win32_getvolumepathnamesforvolumename","base.getvolumepathnamesforvolumename","fileapi/GetVolumePathNamesForVolumeName","fileapi/GetVolumePathNamesForVolumeNameA","fileapi/GetVolumePathNamesForVolumeNameW","fs.getvolumepathnamesforvolumename","winbase/GetVolumePathNamesForVolumeName","winbase/GetVolumePathNamesForVolumeNameA","winbase/GetVolumePathNamesForVolumeNameW"]
old-location: fs\getvolumepathnamesforvolumename.htm
tech.root: fs
ms.assetid: 067904c1-d3e1-4cfd-ac63-6ef32d9a2513
ms.date: 12/05/2018
ms.keywords: GetVolumePathNamesForVolumeName, GetVolumePathNamesForVolumeName function [Files], GetVolumePathNamesForVolumeNameA, GetVolumePathNamesForVolumeNameW, _win32_getvolumepathnamesforvolumename, base.getvolumepathnamesforvolumename, fileapi/GetVolumePathNamesForVolumeName, fileapi/GetVolumePathNamesForVolumeNameA, fileapi/GetVolumePathNamesForVolumeNameW, fs.getvolumepathnamesforvolumename, winbase/GetVolumePathNamesForVolumeName, winbase/GetVolumePathNamesForVolumeNameA, winbase/GetVolumePathNamesForVolumeNameW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetVolumePathNamesForVolumeNameW (Unicode) and GetVolumePathNamesForVolumeNameA (ANSI)
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
 - GetVolumePathNamesForVolumeNameW
 - fileapi/GetVolumePathNamesForVolumeNameW
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
 - GetVolumePathNamesForVolumeName
 - GetVolumePathNamesForVolumeNameA
 - GetVolumePathNamesForVolumeNameW
---

# GetVolumePathNamesForVolumeNameW function


## -description

Retrieves a list of drive letters and mounted folder paths for the specified volume.

## -parameters

### -param lpszVolumeName [in]

A volume <b>GUID</b> path for the volume. A volume <b>GUID</b> 
      path is of the form 
      "\\\\?\\Volume{<i>xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx</i>}\\".

### -param lpszVolumePathNames [out]

A pointer to a buffer that receives the list of drive letters and mounted folder paths. The list is an 
      array of null-terminated strings terminated by an additional <b>NULL</b> character. If the 
      buffer is not large enough to hold the complete list, the buffer holds as much of the list as possible.

### -param cchBufferLength [in]

The length of the <i>lpszVolumePathNames</i> buffer, in 
      <b>WCHARs</b>, including all <b>NULL</b> characters.

### -param lpcchReturnLength [out]

If the call is successful, this parameter is the number of <b>WCHARs</b> copied to 
      the <i>lpszVolumePathNames</i> buffer. Otherwise, this parameter is the size of the buffer 
      required to hold the complete list, in <b>WCHARs</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If the buffer is not large enough to 
       hold the complete list, the error code is <b>ERROR_MORE_DATA</b> and the 
       <i>lpcchReturnLength</i> parameter receives the required buffer size.

## -remarks

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

<a href="/windows/desktop/FileIO/volume-mount-points">Mounted Folders</a>



<a href="/windows/desktop/FileIO/volume-management-functions">Volume Management Functions</a>
