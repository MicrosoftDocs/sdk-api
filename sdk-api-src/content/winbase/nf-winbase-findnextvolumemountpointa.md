---
UID: NF:winbase.FindNextVolumeMountPointA
title: FindNextVolumeMountPointA function (winbase.h)
description: Continues a mounted folder search started by a call to the FindFirstVolumeMountPoint function. (ANSI)
helpviewer_keywords: ["FindNextVolumeMountPointA", "winbase/FindNextVolumeMountPointA"]
old-location: fs\findnextvolumemountpoint.htm
tech.root: fs
ms.assetid: 299e2fed-74d8-4008-b593-981c52016532
ms.date: 12/05/2018
ms.keywords: FindNextVolumeMountPoint, FindNextVolumeMountPoint function [Files], FindNextVolumeMountPointA, FindNextVolumeMountPointW, _win32_findnextvolumemountpoint, base.findnextvolumemountpoint, fs.findnextvolumemountpoint, winbase/FindNextVolumeMountPoint, winbase/FindNextVolumeMountPointA, winbase/FindNextVolumeMountPointW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindNextVolumeMountPointW (Unicode) and FindNextVolumeMountPointA (ANSI)
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
 - FindNextVolumeMountPointA
 - winbase/FindNextVolumeMountPointA
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
 - FindNextVolumeMountPoint
 - FindNextVolumeMountPointA
 - FindNextVolumeMountPointW
---

# FindNextVolumeMountPointA function


## -description

Continues a mounted folder search started by a call to the 
    <a href="/windows/desktop/api/winbase/nf-winbase-findfirstvolumemountpointa">FindFirstVolumeMountPoint</a> 
    function. <b>FindNextVolumeMountPoint</b> finds one mounted 
    folder per call.

## -parameters

### -param hFindVolumeMountPoint [in]

A mounted folder search handle returned by a previous call to the 
      <a href="/windows/desktop/api/winbase/nf-winbase-findfirstvolumemountpointa">FindFirstVolumeMountPoint</a> function.

### -param lpszVolumeMountPoint [out]

A pointer to a buffer that receives the name of the mounted folder that is found.

### -param cchBufferLength [in]

The length of the buffer that receives the mounted folder name, in 
      <b>TCHARs</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. If no more mounted folders can be found, 
       the <b>GetLastError</b> function returns the 
       <b>ERROR_NO_MORE_FILES</b> error code. In that case, close the search with the 
       <a href="/windows/desktop/api/winbase/nf-winbase-findvolumemountpointclose">FindVolumeMountPointClose</a> function.

## -remarks

After the search handle is established by calling 
    <a href="/windows/desktop/api/winbase/nf-winbase-findfirstvolumemountpointa">FindFirstVolumeMountPoint</a>, you can 
    use the <b>FindNextVolumeMountPoint</b> function to 
    search for other mounted folders.

The <a href="/windows/desktop/api/winbase/nf-winbase-findfirstvolumemountpointa">FindFirstVolumeMountPoint</a>, 
    <b>FindNextVolumeMountPoint</b>, and 
    <a href="/windows/desktop/api/winbase/nf-winbase-findvolumemountpointclose">FindVolumeMountPointClose</a> functions return 
    paths to mounted folders for a specified volume. They do not return drive letters or volume GUID paths. For 
    information about enumerating the volume <b>GUID</b> paths for a volume, see 
    <a href="/windows/desktop/FileIO/enumerating-unique-volume-names">Enumerating Volume GUID Paths</a>.

You should not assume any correlation between the order of the mounted folders that are returned with these 
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
> The winbase.h header defines FindNextVolumeMountPoint as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-findfirstvolumemountpointa">FindFirstVolumeMountPoint</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findvolumemountpointclose">FindVolumeMountPointClose</a>



<a href="/windows/desktop/FileIO/volume-mount-points">Mounted Folders</a>



<a href="/windows/desktop/FileIO/volume-management-functions">Volume Management Functions</a>
