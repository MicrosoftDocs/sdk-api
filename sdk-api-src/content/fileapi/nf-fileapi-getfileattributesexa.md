---
UID: NF:fileapi.GetFileAttributesExA
title: GetFileAttributesExA function (fileapi.h)
description: Retrieves attributes for a specified file or directory. (ANSI)
helpviewer_keywords: ["GetFileAttributesExA", "GetFileExInfoStandard", "fileapi/GetFileAttributesExA"]
old-location: fs\getfileattributesex.htm
tech.root: fs
ms.assetid: e5d84000-17c1-4517-97a7-6bd240d73814
ms.date: 12/05/2018
ms.keywords: GetFileAttributesEx, GetFileAttributesEx function [Files], GetFileAttributesExA, GetFileAttributesExW, GetFileExInfoStandard, _win32_getfileattributesex, base.getfileattributesex, fileapi/GetFileAttributesEx, fileapi/GetFileAttributesExA, fileapi/GetFileAttributesExW, fs.getfileattributesex, winbase/GetFileAttributesEx, winbase/GetFileAttributesExA, winbase/GetFileAttributesExW
req.header: fileapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetFileAttributesExW (Unicode) and GetFileAttributesExA (ANSI)
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
 - GetFileAttributesExA
 - fileapi/GetFileAttributesExA
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
 - GetFileAttributesEx
 - GetFileAttributesExA
 - GetFileAttributesExW
---

# GetFileAttributesExA function


## -description

Retrieves attributes for a specified file or directory.

To perform this operation as a transacted operation, use the 
    <a href="/windows/desktop/api/winbase/nf-winbase-getfileattributestransacteda">GetFileAttributesTransacted</a> function.

## -parameters

### -param lpFileName [in]

The name of the file or directory.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.



### -param fInfoLevelId [in]

A class of attribute information to retrieve.

This parameter can be the following value from the 
      <a href="/windows/desktop/api/minwinbase/ne-minwinbase-get_fileex_info_levels">GET_FILEEX_INFO_LEVELS</a> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GetFileExInfoStandard"></a><a id="getfileexinfostandard"></a><a id="GETFILEEXINFOSTANDARD"></a><dl>
<dt><b>GetFileExInfoStandard</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpFileInformation</i> parameter is a 
        <a href="/windows/desktop/api/fileapi/ns-fileapi-win32_file_attribute_data">WIN32_FILE_ATTRIBUTE_DATA</a> 
        structure.

</td>
</tr>
</table>

### -param lpFileInformation [out]

A pointer to a buffer that receives the attribute information.

The type of attribute information that is stored into this buffer is determined by the value of 
       <i>fInfoLevelId</i>.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero (0). To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a> function retrieves file 
    system attribute information. <b>GetFileAttributesEx</b> 
    can obtain other sets of file or directory attribute information. Currently, 
    <b>GetFileAttributesEx</b> retrieves a set of standard 
    attributes that is a superset of the file system attribute information.

When the <b>GetFileAttributesEx</b> function is 
    called on a directory that is a mounted folder, it returns the attributes of the directory, not those of the root 
    directory in the volume that the mounted folder associates with the directory. To obtain the attributes of the 
    associated volume, call 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumenameforvolumemountpointw">GetVolumeNameForVolumeMountPoint</a> to 
    obtain the name of the associated volume. Then use the resulting name in a call to 
    <b>GetFileAttributesEx</b>. The results are the attributes 
    of the root directory on the associated volume.

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
 

Symbolic link behavior—If the path points to a symbolic link, the function returns 
    attributes for the symbolic link.

<h3><a id="Transacted_Operations"></a><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
If a file is open for modification in a transaction, no other thread can open the file for modification until 
      the transaction is committed.  So if a transacted thread opens the file first, any subsequent threads that try 
      modifying the file before the transaction is committed receives a sharing violation.  If a non-transacted thread 
      modifies the file before the transacted thread does, and the file is still open when the transaction attempts to 
      open it, the transaction receives the error <b>ERROR_TRANSACTIONAL_CONFLICT</b>.





> [!NOTE]
> The fileapi.h header defines GetFileAttributesEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getfileattributestransacteda">GetFileAttributesTransacted</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-setfileattributesa">SetFileAttributes</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>
