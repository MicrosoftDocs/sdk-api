---
UID: NF:fileapi.FindNextFileA
title: FindNextFileA function (fileapi.h)
description: Continues a file search from a previous call to the FindFirstFile, FindFirstFileEx, or FindFirstFileTransacted functions. (ANSI)
helpviewer_keywords: ["FindNextFileA", "fileapi/FindNextFileA"]
old-location: fs\findnextfile.htm
tech.root: fs
ms.assetid: db7acb83-2da6-40bf-9962-5cfe54e257a5
ms.date: 12/05/2018
ms.keywords: FindNextFile, FindNextFile function [Files], FindNextFileA, FindNextFileW, _win32_findnextfile, base.findnextfile, fileapi/FindNextFile, fileapi/FindNextFileA, fileapi/FindNextFileW, fs.findnextfile, winbase/FindNextFile, winbase/FindNextFileA, winbase/FindNextFileW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FindNextFileA
 - fileapi/FindNextFileA
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
 - FindNextFile
 - FindNextFileA
 - FindNextFileW
---

# FindNextFileA function


## -description

Continues a file search from a previous call to the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a>, 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfileexa">FindFirstFileEx</a>, or 
    <a href="/windows/desktop/api/winbase/nf-winbase-findfirstfiletransacteda">FindFirstFileTransacted</a> functions.

## -parameters

### -param hFindFile [in]

The search handle returned by a previous call to the 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a> or 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfileexa">FindFirstFileEx</a> function.

### -param lpFindFileData [out]

A pointer to the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> structure 
      that receives information about the found file or subdirectory.

## -returns

If the function succeeds, the return value is nonzero and  the <i>lpFindFileData</i> 
       parameter contains information about the next file or directory found.

If the function fails, the return value is zero and the contents of <i>lpFindFileData</i> 
       are indeterminate. To get extended error information, call the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

If the function fails because no more matching files can be found, the 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns 
       <b>ERROR_NO_MORE_FILES</b>.

## -remarks

This function uses the same search filters that were used to create the search handle passed in the 
    <i>hFindFile</i> parameter. For additional information, see 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a> and 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfileexa">FindFirstFileEx</a>.

The order in which the search returns the files, such as alphabetical order, is not guaranteed, and is 
    dependent on the file system. If the data  must be sorted, 
    the application must do the ordering after obtaining all the results.

<div class="alert"><b>Note</b>  In rare cases or on a heavily loaded system, file attribute information on NTFS file systems may not be 
    current at the time this function is called. To be assured of getting the current NTFS file system file 
    attributes, call the 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileinformationbyhandle">GetFileInformationByHandle</a> function.</div>
<div> </div>
The order in which this function returns the file names is dependent on the file system type. With the NTFS 
    file system and CDFS file systems, the names are usually returned in alphabetical order. With FAT file systems, 
    the names are usually returned in the order the files were written to the disk, which may or may not be in 
    alphabetical order. However, as stated previously, these behaviors are not guaranteed.

If the path points to a symbolic link, the 
    <a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a> buffer contains information about the 
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
     <a href="/windows/desktop/FileIO/listing-the-files-in-a-directory">Listing the Files in a Directory</a>.

<div class="code"></div>




> [!NOTE]
> The fileapi.h header defines FindNextFile as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findclose">FindClose</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfilea">FindFirstFile</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findfirstfileexa">FindFirstFileEx</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileattributesa">SetFileAttributes</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa">WIN32_FIND_DATA</a>
