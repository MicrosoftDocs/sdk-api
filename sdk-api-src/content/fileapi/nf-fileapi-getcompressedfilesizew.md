---
UID: NF:fileapi.GetCompressedFileSizeW
title: GetCompressedFileSizeW function (fileapi.h)
description: Retrieves the actual number of bytes of disk storage used to store a specified file. (Unicode)
helpviewer_keywords: ["GetCompressedFileSize", "GetCompressedFileSize function [Files]", "GetCompressedFileSizeW", "_win32_getcompressedfilesize", "base.getcompressedfilesize", "fileapi/GetCompressedFileSize", "fileapi/GetCompressedFileSizeW", "fs.getcompressedfilesize"]
old-location: fs\getcompressedfilesize.htm
tech.root: fs
ms.assetid: cca91080-2270-4996-8693-933c585ff168
ms.date: 12/05/2018
ms.keywords: GetCompressedFileSize, GetCompressedFileSize function [Files], GetCompressedFileSizeA, GetCompressedFileSizeW, _win32_getcompressedfilesize, base.getcompressedfilesize, fileapi/GetCompressedFileSize, fileapi/GetCompressedFileSizeA, fileapi/GetCompressedFileSizeW, fs.getcompressedfilesize
req.header: fileapi.h
req.include-header: Windows.h, WinBase.h, Fileapi.h, Windows.h, WinBase.h, Fileapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetCompressedFileSizeW (Unicode) and GetCompressedFileSizeA (ANSI)
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
 - GetCompressedFileSizeW
 - fileapi/GetCompressedFileSizeW
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
 - API-MS-Win-Core-File-l1-2-1.dll
 - KernelBase.dll
 - API-MS-Win-Core-File-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetCompressedFileSize
 - GetCompressedFileSizeA
 - GetCompressedFileSizeW
---

# GetCompressedFileSizeW function


## -description

Retrieves the actual number of bytes of disk storage used to store a specified file. If the file is located on a volume that supports compression and the file is compressed, the value obtained is the compressed size of the specified file. If the file is located on a volume that supports sparse files and the file is a sparse file, the value obtained is the sparse size of the specified file.

To perform this operation as a transacted operation, use the <a href="/windows/desktop/api/winbase/nf-winbase-getcompressedfilesizetransacteda">GetCompressedFileSizeTransacted</a> function.

## -parameters

### -param lpFileName [in]

The name of the file. 




Do not specify the name of a file on a nonseeking device, such as a pipe or a communications device, as its file size has no meaning.

This parameter may include the path. 

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param lpFileSizeHigh [out, optional]

The high-order <b>DWORD</b> of the compressed file size. The function's return value is the low-order <b>DWORD</b> of the compressed file size. 




This parameter can be <b>NULL</b> if the high-order <b>DWORD</b> of the compressed file size is not needed. Files less than 4 gigabytes in size do not need the high-order <b>DWORD</b>.

## -returns

If the function succeeds, the return value is the low-order <b>DWORD</b> of the actual number of bytes of disk storage used to store the specified file, and if <i>lpFileSizeHigh</i> is non-<b>NULL</b>, the function puts the high-order <b>DWORD</b> of that actual value into the <b>DWORD</b> pointed to by that parameter. This is the compressed file size for compressed files, the actual file size for noncompressed files.

If the function fails, and <i>lpFileSizeHigh</i> is <b>NULL</b>, the return value is <b>INVALID_FILE_SIZE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

If the return value is <b>INVALID_FILE_SIZE</b> and <i>lpFileSizeHigh</i> is non-<b>NULL</b>, an application must call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to determine whether the function has succeeded (value is <b>NO_ERROR</b>) or failed (value is other than <b>NO_ERROR</b>).

## -remarks

An application can determine whether a volume is compressed by calling 
<a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa">GetVolumeInformation</a>, then checking the status of the <b>FS_VOL_IS_COMPRESSED</b> flag in the <b>DWORD</b> value pointed to by that function's <i>lpFileSystemFlags</i> parameter.

If the file is not located on a volume that supports compression or sparse files, or if the file is not compressed or a sparse file, the value obtained is the actual file size, the same as the value returned by a call to 
<a href="/windows/desktop/api/fileapi/nf-fileapi-getfilesize">GetFileSize</a>.

Symbolic link behavior—If the path points to a symbolic link, the function returns the file size of the target.

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
 





> [!NOTE]
> The fileapi.h header defines GetCompressedFileSize as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-compression-and-decompression">File Compression and Decompression</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getcompressedfilesizetransacteda">GetCompressedFileSizeTransacted</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfilesize">GetFileSize</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa">GetVolumeInformation</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>
