---
UID: NF:winbase.GetFileAttributesTransactedA
title: GetFileAttributesTransactedA function (winbase.h)
description: Retrieves file system attributes for a specified file or directory as a transacted operation. (ANSI)
helpviewer_keywords: ["GetFileAttributesTransactedA", "GetFileExInfoStandard", "winbase/GetFileAttributesTransactedA"]
old-location: fs\getfileattributestransacted.htm
tech.root: fs
ms.assetid: dd1435da-93e5-440a-913a-9e40e39b4a01
ms.date: 12/05/2018
ms.keywords: GetFileAttributesTransacted, GetFileAttributesTransacted function [Files], GetFileAttributesTransactedA, GetFileAttributesTransactedW, GetFileExInfoStandard, fs.getfileattributestransacted, winbase/GetFileAttributesTransacted, winbase/GetFileAttributesTransactedA, winbase/GetFileAttributesTransactedW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetFileAttributesTransactedW (Unicode) and GetFileAttributesTransactedA (ANSI)
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
 - GetFileAttributesTransactedA
 - winbase/GetFileAttributesTransactedA
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
 - GetFileAttributesTransacted
 - GetFileAttributesTransactedA
 - GetFileAttributesTransactedW
---

# GetFileAttributesTransactedA function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Retrieves file system attributes for a specified file or directory as a transacted 
    operation.

## -parameters

### -param lpFileName [in]

The name of the file or directory.
      

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

The file or directory must reside on the local computer; otherwise, the function fails and the last error code is set to <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.

### -param fInfoLevelId [in]

The level of attribute information to retrieve.
      

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
       <i>fInfoLevelId</i>. If the <i>fInfoLevelId</i> parameter is 
       <b>GetFileExInfoStandard</b> then this parameter points to a 
       <a href="/windows/desktop/api/fileapi/ns-fileapi-win32_file_attribute_data">WIN32_FILE_ATTRIBUTE_DATA</a> 
        structure

### -param hTransaction [in]

A handle to the transaction. This handle is returned by the <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended 
       error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When <b>GetFileAttributesTransacted</b> is 
    called on a directory that is a mounted folder, it returns the attributes of the directory, not those of the root directory in the volume that the mounted folder associates with the directory. To obtain the 
    file attributes of the associated volume, call 
    <a href="/windows/desktop/api/fileapi/nf-fileapi-getvolumenameforvolumemountpointw">GetVolumeNameForVolumeMountPoint</a> to 
    obtain the name of the associated volume. Then use the resulting name in a call to 
    <b>GetFileAttributesTransacted</b>. The results are 
    the attributes of the root directory on the associated volume.

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

<b>Symbolic links:  </b>If the path points to a symbolic link, the function returns attributes for the symbolic link.

<h3><a id="Transacted_Operations"></a><a id="transacted_operations"></a><a id="TRANSACTED_OPERATIONS"></a>Transacted Operations</h3>
If a file is open for modification in a transaction, no other thread can open the file for modification until 
      the transaction is committed. Conversely, if a file is open for modification outside of a transaction, no 
      transacted thread can open the file for modification until the non-transacted handle is closed. If a 
      non-transacted thread has a handle opened to modify a file, a call to 
      <b>GetFileAttributesTransacted</b> for that file 
      will fail with an <b>ERROR_TRANSACTIONAL_CONFLICT</b> error.





> [!NOTE]
> The winbase.h header defines GetFileAttributesTransacted as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>



<a href="/windows/desktop/FileIO/file-attribute-constants">File Attribute Constants</a>



<a href="/windows/desktop/FileIO/file-management-functions">File Management Functions</a>



<a href="/windows/desktop/api/winbase/nf-winbase-findfirstfiletransacteda">FindFirstFileTransacted</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-findnextfilea">FindNextFile</a>



<a href="/windows/desktop/api/minwinbase/ne-minwinbase-get_fileex_info_levels">GET_FILEEX_INFO_LEVELS</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setfileattributestransacteda">SetFileAttributesTransacted</a>



<a href="/windows/desktop/FileIO/symbolic-links">Symbolic Links</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>
