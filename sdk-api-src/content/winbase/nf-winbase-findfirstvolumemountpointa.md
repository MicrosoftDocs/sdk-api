---
UID: NF:winbase.FindFirstVolumeMountPointA
title: FindFirstVolumeMountPointA function (winbase.h)
description: Retrieves the name of a mounted folder on the specified volume. (ANSI)
helpviewer_keywords: ["FindFirstVolumeMountPointA", "winbase/FindFirstVolumeMountPointA"]
old-location: fs\findfirstvolumemountpoint.htm
tech.root: fs
ms.assetid: 2ac3c22d-b8dd-43d8-a7af-877b54e42d9d
ms.date: 12/05/2018
ms.keywords: FindFirstVolumeMountPoint, FindFirstVolumeMountPoint function [Files], FindFirstVolumeMountPointA, FindFirstVolumeMountPointW, _win32_findfirstvolumemountpoint, base.findfirstvolumemountpoint, fs.findfirstvolumemountpoint, winbase/FindFirstVolumeMountPoint, winbase/FindFirstVolumeMountPointA, winbase/FindFirstVolumeMountPointW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindFirstVolumeMountPointW (Unicode) and FindFirstVolumeMountPointA (ANSI)
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
 - FindFirstVolumeMountPointA
 - winbase/FindFirstVolumeMountPointA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - FindFirstVolumeMountPoint
 - FindFirstVolumeMountPointA
 - FindFirstVolumeMountPointW
---

# FindFirstVolumeMountPointA function


## -description

Retrieves the name of a mounted folder on the specified volume. <b>FindFirstVolumeMountPoint</b> is used to begin scanning the mounted folders on a 
    volume.

## -parameters

### -param lpszRootPathName [in]

A volume GUID path for the volume to scan for mounted folders. A trailing backslash is required.

### -param lpszVolumeMountPoint [out]

A pointer to a buffer that receives the name of the first mounted folder that is found.

### -param cchBufferLength [in]

The length of the buffer that receives the path to the mounted folder, in 
      <b>TCHAR</b>s.

## -returns

If the function succeeds, the return value is a search handle used in a subsequent call to the 
       <a href="/windows/desktop/api/winbase/nf-winbase-findnextvolumemountpointa">FindNextVolumeMountPoint</a> and 
       <a href="/windows/desktop/api/winbase/nf-winbase-findvolumemountpointclose">FindVolumeMountPointClose</a> functions.

If the function fails to find a mounted folder on the volume, the return value is the 
       <b>INVALID_HANDLE_VALUE</b> error code. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>FindFirstVolumeMountPoint</b> function 
    opens a mounted folder search handle and returns information about the first mounted folder that is found on the 
    specified volume. After the search handle is established, you can use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-findnextvolumemountpointa">FindNextVolumeMountPoint</a> function to search for 
    other mounted folders. When the search handle is no longer needed, close it with the 
    <a href="/windows/desktop/api/winbase/nf-winbase-findvolumemountpointclose">FindVolumeMountPointClose</a> function.

The <b>FindFirstVolumeMountPoint</b>, 
    <a href="/windows/desktop/api/winbase/nf-winbase-findnextvolumemountpointa">FindNextVolumeMountPoint</a>, and 
    <a href="/windows/desktop/api/winbase/nf-winbase-findvolumemountpointclose">FindVolumeMountPointClose</a> functions return 
    paths to mounted folders for a specified volume. They do not return drive letters or volume 
    <b>GUID</b> paths. For information about enumerating the volume 
    <b>GUID</b> paths for a volume, see 
    <a href="/windows/desktop/FileIO/enumerating-unique-volume-names">Enumerating Volume GUID Paths</a>.

You should not assume any correlation between the order of the mounted folders that are returned by these 
    functions and the order of the mounted folders that are returned by other functions or tools.

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
 

SMB does not support volume management functions. CsvFS does not support adding mount point on a CSV volume. 
     ReFS does not index mount points.





> [!NOTE]
> The winbase.h header defines FindFirstVolumeMountPoint as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-findnextvolumemountpointa">FindNextVolumeMountPoint</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findvolumemountpointclose">FindVolumeMountPointClose</a>



<a href="/windows/desktop/FileIO/volume-mount-points">Mounted Folders</a>



<a href="/windows/desktop/FileIO/volume-management-functions">Volume Management Functions</a>
