---
UID: NF:fileapi.FindNextFileW
title: FindNextFileW function
author: windows-sdk-content
description: Continues a file search from a previous call to the FindFirstFile, FindFirstFileEx, or FindFirstFileTransacted functions.
old-location: fs\findnextfile.htm
tech.root: FileIO
ms.assetid: db7acb83-2da6-40bf-9962-5cfe54e257a5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: FindNextFile, FindNextFile function [Files], FindNextFileA, FindNextFileW, _win32_findnextfile, base.findnextfile, fileapi/FindNextFile, fileapi/FindNextFileA, fileapi/FindNextFileW, fs.findnextfile, winbase/FindNextFile, winbase/FindNextFileA, winbase/FindNextFileW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FindNextFileW (Unicode) and FindNextFileA (ANSI)
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
api_name:
 - FindNextFile
 - FindNextFileA
 - FindNextFileW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FindNextFileW function


## -description


Continues a file search from a previous call to the 
    <a href="https://msdn.microsoft.com/02fc92c4-582d-4c9f-a811-b5c839e9fffa">FindFirstFile</a>, 
    <a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a>, or 
    <a href="https://msdn.microsoft.com/d94bf32b-f14b-44b4-824b-ed453d0424ef">FindFirstFileTransacted</a> functions.


## -parameters




### -param hFindFile [in]

The search handle returned by a previous call to the 
      <a href="https://msdn.microsoft.com/02fc92c4-582d-4c9f-a811-b5c839e9fffa">FindFirstFile</a> or 
      <a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a> function.


### -param lpFindFileData [out]

A pointer to the <a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a> structure 
      that receives information about the found file or subdirectory.


## -returns



If the function succeeds, the return value is nonzero and  the <i>lpFindFileData</i> 
       parameter contains information about the next file or directory found.

If the function fails, the return value is zero and the contents of <i>lpFindFileData</i> 
       are indeterminate. To get extended error information, call the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.

If the function fails because no more matching files can be found, the 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns 
       <b>ERROR_NO_MORE_FILES</b>.




## -remarks



This function uses the same search filters that were used to create the search handle passed in the 
    <i>hFindFile</i> parameter. For additional information, see 
    <a href="https://msdn.microsoft.com/02fc92c4-582d-4c9f-a811-b5c839e9fffa">FindFirstFile</a> and 
    <a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a>.

The order in which the search returns the files, such as alphabetical order, is not guaranteed, and is 
    dependent on the file system. If the data  must be sorted, 
    the application must do the ordering after obtaining all the results.

<div class="alert"><b>Note</b>  In rare cases or on a heavily loaded system, file attribute information on NTFS file systems may not be 
    current at the time this function is called. To be assured of getting the current NTFS file system file 
    attributes, call the 
    <a href="https://msdn.microsoft.com/d026ee3a-c165-42a2-a4e1-efccdafbefc5">GetFileInformationByHandle</a> function.</div>
<div> </div>
The order in which this function returns the file names is dependent on the file system type. With the NTFS 
    file system and CDFS file systems, the names are usually returned in alphabetical order. With FAT file systems, 
    the names are usually returned in the order the files were written to the disk, which may or may not be in 
    alphabetical order. However, as stated previously, these behaviors are not guaranteed.

If the path points to a symbolic link, the 
    <a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a> buffer contains information about the 
    symbolic link, not the target.

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
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 Transparent Failover (TFO)

</td>
<td>
Yes

</td>
</tr>
<tr>
<td>
SMB 3.0 with Scale-out File Shares (SO)

</td>
<td>
Yes

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
 

<h3><a id="Transacted_Operations"></a><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
If there is a transaction bound to the file enumeration handle, then the files that are returned are subject 
      to transaction isolation rules.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/ab0d977d-f71c-4a18-9b1d-2221169324f0">Listing the Files in a Directory</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/64b3bc49-1e0e-4572-9d9f-936c45f5b01c">FindClose</a>



<a href="https://msdn.microsoft.com/02fc92c4-582d-4c9f-a811-b5c839e9fffa">FindFirstFile</a>



<a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a>



<a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a>



<a href="https://msdn.microsoft.com/3d5400c3-555f-44fc-9470-52a36d04d90b">SetFileAttributes</a>



<a href="https://msdn.microsoft.com/d6bf5df7-bc12-4dec-b116-95d9109f5eb4">Symbolic Links</a>



<a href="https://msdn.microsoft.com/eb700d84-0ba5-4af8-a619-2d2544560dbc">WIN32_FIND_DATA</a>
 

 

