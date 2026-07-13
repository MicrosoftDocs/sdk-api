---
UID: NF:winbase.GetVolumePathNameA
title: GetVolumePathNameA function (winbase.h)
description: Retrieves the volume mount point where the specified path is mounted. (GetVolumePathNameA)
helpviewer_keywords: ["GetVolumePathName","GetVolumePathName function [Files]","GetVolumePathNameA","GetVolumePathNameW","_win32_getvolumepathname","base.getvolumepathname","fileapi/GetVolumePathName","fileapi/GetVolumePathNameA","fileapi/GetVolumePathNameW","fs.getvolumepathname","winbase/GetVolumePathName","winbase/GetVolumePathNameA","winbase/GetVolumePathNameW"]
old-location: fs\getvolumepathname.htm
tech.root: fs
ms.assetid: fa34786c-af82-4b59-bf36-e9a95a2f913e
ms.date: 12/05/2018
ms.keywords: GetVolumePathName, GetVolumePathName function [Files], GetVolumePathNameA, GetVolumePathNameW, _win32_getvolumepathname, base.getvolumepathname, fileapi/GetVolumePathName, fileapi/GetVolumePathNameA, fileapi/GetVolumePathNameW, fs.getvolumepathname, winbase/GetVolumePathName, winbase/GetVolumePathNameA, winbase/GetVolumePathNameW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetVolumePathNameW (Unicode) and GetVolumePathNameA (ANSI)
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
 - GetVolumePathNameA
 - winbase/GetVolumePathNameA
dev_langs:
 - c++
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
 - GetVolumePathName
 - GetVolumePathNameA
 - GetVolumePathNameW
---

# GetVolumePathNameA function


## -description

Retrieves the volume mount point where the specified path is mounted.

## -parameters

### -param lpszFileName [in]

A pointer to the input path string. Both absolute and relative file and directory names, for example 
       "..", are acceptable in this path.

If you specify a relative directory or file name without a volume qualifier, 
       <b>GetVolumePathName</b> returns the drive letter of the 
       boot volume.

If this parameter is an empty string, "", the function fails but the last error is set to 
       <b>ERROR_SUCCESS</b>.

### -param lpszVolumePathName [out]

A pointer to a string that receives the volume mount point for the input path.

### -param cchBufferLength [in]

The length of the output buffer, in <b>TCHARs</b>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If a specified path is passed, <b>GetVolumePathName</b> 
    returns the path to the volume mount point, which means that it returns the root of the volume where the end point 
    of the specified path is located.

For example, assume that you have volume D mounted at C:\Mnt\Ddrive 
    and volume E mounted at "C:\Mnt\Ddrive\Mnt\Edrive". Also assume that you 
    have a file with the path "E:\Dir\Subdir\MyFile". If you pass 
    "C:\Mnt\Ddrive\Mnt\Edrive\Dir\Subdir\MyFile" to 
    <b>GetVolumePathName</b>, it returns the path 
    "C:\Mnt\Ddrive\Mnt\Edrive\".

If either a relative directory or a file is passed without a volume qualifier, the function returns the drive 
    letter of the boot volume. The drive letter of the boot volume is also returned if an invalid file or directory 
    name is specified without a valid volume qualifier. If a valid volume specifier is given, and the volume exists, 
    but an invalid file or directory name is specified, the function will succeed and that volume name will be 
    returned. For examples, see the Examples section of this topic.

You must specify a valid Win32 namespace path. If you specify an NT namespace path, for example, 
    "\DosDevices\H:" or 
    "\Device\HardDiskVolume6", the function returns the drive letter of the 
    boot volume, not the drive letter of that NT namespace path.

For more information about path names and namespaces, see 
    <a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a>.

You can specify both local and remote paths. If you specify a local path, 
    <b>GetVolumePathName</b> returns a full path whose prefix is 
    the longest prefix that represents a volume.

If a network share is specified, <b>GetVolumePathName</b> 
    returns the shortest path for which <a href="/windows/desktop/api/fileapi/nf-fileapi-getdrivetypea">GetDriveType</a> returns 
    <b>DRIVE_REMOTE</b>, which means that the path is validated as a remote drive that exists, 
    which the current user can access.

There are certain special cases that do not return a trailing backslash. These occur when the output buffer 
    length is one character too short. For example, if <i>lpszFileName</i> is 
    C: and <i>lpszVolumePathName</i> is 4 characters long, the value 
    returned is "C:\"; however, if 
    <i>lpszVolumePathName</i> is 3 characters long, the value returned is 
    "C:". A safer but slower way to set the size of the return buffer is to 
    call the <a href="/windows/desktop/api/fileapi/nf-fileapi-getfullpathnamea">GetFullPathName</a> function, and then make sure 
    that the buffer size is at least the same size as the full path that 
    <b>GetFullPathName</b> returns. If the output buffer is more 
    than one character too short, the function will fail and return an error.

In Windows 8 and Windows Server 2012, this function is supported by the following 
    technologies.

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

<h3><a id="Trailing_Path_Elements"></a><a id="trailing_path_elements"></a><a id="TRAILING_PATH_ELEMENTS"></a>Trailing Path Elements</h3>
Trailing path elements that are invalid are ignored. For remote paths, the entire path (not just trailing 
      elements) is considered invalid if one of the following conditions is true: 
      <ul>
<li>The path is not formed correctly.</li>
<li>The path does not exist.</li>
<li>The current user does not have access to the path.</li>
</ul>


<h3><a id="Junction_Points_and_Mounted_Folders"></a><a id="junction_points_and_mounted_folders"></a><a id="JUNCTION_POINTS_AND_MOUNTED_FOLDERS"></a>Junction Points and Mounted Folders</h3>
If the specified path traverses a junction point, 
      <b>GetVolumePathName</b> returns the volume to which the 
      junction point refers. For example, if <code>W:\Adir</code> is a junction point 
      that points to <code>C:\Adir</code>, then 
      <b>GetVolumePathName</b> invoked on 
      <code>W:\Adir\Afile</code> returns "<code>C:\</code>". 
      If the specified path traverses multiple junction points, the entire chain is followed, and 
      <b>GetVolumePathName</b> returns the volume to which the 
      last junction point in the chain refers.

If a remote path to a mounted folder or junction point is specified, the path is parsed as a remote path, and 
      the mounted folder or junction point are ignored. For example if 
      <code>C:\Dir_C</code> is linked to 
      <code>D:\Dir_D</code> and <code>C:</code> is mapped to 
      <code>X:</code> on a remote computer, calling 
      <b>GetVolumePathName</b> and specifying 
      <code>X:\Dir_C</code> on the remote computer returns 
      <code>X:\</code>.


#### Examples

For the following set of examples, U: is mapped to the remote computer 
     &#92;&#92;<i>YourComputer</i>\C$, and Q is a local drive.
     

<table>
<tr>
<th>Specified path</th>
<th>Function returns</th>
</tr>
<tr>
<td>&#92;&#92;<i>YourComputer</i>\C$\Windows</td>
<td>&#92;&#92;<i>YourComputer</i>\C$\</td>
</tr>
<tr>
<td>\\?\UNC&#92;<i>YourComputer</i>\C$\Windows</td>
<td>\\?\UNC&#92;<i>YourComputer</i>\C$\</td>
</tr>
<tr>
<td>Q:\Windows</td>
<td>Q:\</td>
</tr>
<tr>
<td>\\?\Q:\Windows</td>
<td>\\?\Q:\</td>
</tr>
<tr>
<td>\\.\Q:\Windows</td>
<td>\\.\Q:\</td>
</tr>
<tr>
<td>\\?\UNC\W:\Windows</td>
<td><b>FALSE</b> with error 123 because a specified remote path was not valid; 
        W$ share does not exist or no user access granted.</td>
</tr>
<tr>
<td>C:\COM2 (which exists)</td>
<td>\\.\COM2\</td>
</tr>
<tr>
<td>C:\COM3 (non-existent)</td>
<td><b>FALSE</b> with error 123 because a non-existent COM device was specified.</td>
</tr>
</table>
 

<div class="code"></div>
For the following set of examples, the paths contain invalid trailing path elements.
     

<table>
<tr>
<th>Specified path</th>
<th>Function returns</th>
</tr>
<tr>
<td>G:\invalid (invalid path)</td>
<td>G:\</td>
</tr>
<tr>
<td>\\.\I:\aaa\invalid (invalid path)</td>
<td>\\.\I:\</td>
</tr>
<tr>
<td>&#92;&#92;<i>YourComputer</i>\C$\invalid (invalid trailing path 
        element)</td>
<td>&#92;&#92;<i>YourComputer</i>\C$\</td>
</tr>
</table>
 

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-deletevolumemountpointw">DeleteVolumeMountPoint</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfullpathnamea">GetFullPathName</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumenameforvolumemountpointw">GetVolumeNameForVolumeMountPoint</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setvolumemountpointa">SetVolumeMountPoint</a>



<a href="/windows/desktop/FileIO/volume-management-functions">Volume Management Functions</a>



<a href="/windows/desktop/FileIO/volume-mount-points">Volume Mount Points</a>
