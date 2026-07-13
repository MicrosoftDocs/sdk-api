---
UID: NF:winbase.GetCompressedFileSizeTransactedW
title: GetCompressedFileSizeTransactedW function (winbase.h)
description: Retrieves the actual number of bytes of disk storage used to store a specified file as a transacted operation. (Unicode)
helpviewer_keywords: ["GetCompressedFileSizeTransacted", "GetCompressedFileSizeTransacted function [Files]", "GetCompressedFileSizeTransactedW", "fs.getcompressedfilesizetransacted", "winbase/GetCompressedFileSizeTransacted", "winbase/GetCompressedFileSizeTransactedW"]
old-location: fs\getcompressedfilesizetransacted.htm
tech.root: fs
ms.assetid: df062eb4-70e1-4ee7-b489-624938af7834
ms.date: 12/05/2018
ms.keywords: GetCompressedFileSizeTransacted, GetCompressedFileSizeTransacted function [Files], GetCompressedFileSizeTransactedA, GetCompressedFileSizeTransactedW, fs.getcompressedfilesizetransacted, winbase/GetCompressedFileSizeTransacted, winbase/GetCompressedFileSizeTransactedA, winbase/GetCompressedFileSizeTransactedW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetCompressedFileSizeTransactedW (Unicode) and GetCompressedFileSizeTransactedA (ANSI)
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
 - GetCompressedFileSizeTransactedW
 - winbase/GetCompressedFileSizeTransactedW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - Kernel32Legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetCompressedFileSizeTransacted
 - GetCompressedFileSizeTransactedA
 - GetCompressedFileSizeTransactedW
---

# GetCompressedFileSizeTransactedW function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Retrieves the actual number of bytes of disk storage used to store a specified file as a transacted operation. If the file is located on a volume that supports compression and the file is compressed, the value obtained is the compressed size of the specified file. If the file is located on a volume that supports sparse files and the file is a sparse file, the value obtained is the sparse size of the specified file.

## -parameters

### -param lpFileName [in]

The name of the file. 




Do not specify the name of a file on a nonseeking device, such as a pipe or a communications device, as its file size has no meaning.

The file must reside on the local computer; otherwise, the function fails and the last error code is set to <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.

### -param lpFileSizeHigh [out, optional]

A pointer to a variable that receives the high-order <b>DWORD</b> of the compressed file size. The function's return value is the low-order <b>DWORD</b> of the compressed file size. 




This parameter can be <b>NULL</b> if the high-order <b>DWORD</b> of the compressed file size is not needed. Files less than 4 gigabytes in size do not need the high-order <b>DWORD</b>.

### -param hTransaction [in]

A handle to the transaction. This handle is returned by the <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

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

<b>Symbolic links:  </b>If the path points to a symbolic link, the function returns the file size of the target.

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
 

SMB 3.0 does not support TxF.





> [!NOTE]
> The winbase.h header defines GetCompressedFileSizeTransacted as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/FileIO/file-compression-and-decompression">File Compression and Decompression</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getfilesize">GetFileSize</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumeinformationa">GetVolumeInformation</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transaction Management</a>
