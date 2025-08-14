---
UID: NF:winbase.RemoveDirectoryTransactedW
title: RemoveDirectoryTransactedW function (winbase.h)
description: Deletes an existing empty directory as a transacted operation. (Unicode)
helpviewer_keywords: ["RemoveDirectoryTransacted", "RemoveDirectoryTransacted function [Files]", "RemoveDirectoryTransactedW", "fs.removedirectorytransacted", "winbase/RemoveDirectoryTransacted", "winbase/RemoveDirectoryTransactedW"]
old-location: fs\removedirectorytransacted.htm
tech.root: fs
ms.assetid: e8600166-62dc-4398-9e16-43b07f7f0b89
ms.date: 12/05/2018
ms.keywords: RemoveDirectoryTransacted, RemoveDirectoryTransacted function [Files], RemoveDirectoryTransactedA, RemoveDirectoryTransactedW, fs.removedirectorytransacted, winbase/RemoveDirectoryTransacted, winbase/RemoveDirectoryTransactedA, winbase/RemoveDirectoryTransactedW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RemoveDirectoryTransactedW (Unicode) and RemoveDirectoryTransactedA (ANSI)
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
 - RemoveDirectoryTransactedW
 - winbase/RemoveDirectoryTransactedW
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
 - Ext-MS-Win-Kernel32-Transacted-l1-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - Kernel32Legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - RemoveDirectoryTransacted
 - RemoveDirectoryTransactedA
 - RemoveDirectoryTransactedW
---

# RemoveDirectoryTransactedW function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Deletes an existing empty directory as a transacted operation.

## -parameters

### -param lpPathName [in]

The path of the directory to be removed. The path must specify an empty directory, and the calling process 
       must have delete access to the directory.

The directory must reside on the local computer; otherwise, the function fails and the last error code is set 
       to <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.

By default, the name is limited to MAX_PATH characters. To extend this limit to 32,767 wide characters, prepend "\\\\?\\" to the path. For more information, see [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file).

> [!TIP]
> Starting with Windows 10, Version 1607, you can opt-in to remove the MAX_PATH limitation without prepending "\\\\?\\". See the "Maximum Path Length Limitation" section of [Naming Files, Paths, and Namespaces](/windows/win32/fileio/naming-a-file) for details.

### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
      <a href="/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The <b>RemoveDirectoryTransacted</b> function 
    marks a directory for deletion on close. Therefore, the directory is not removed until the last handle to the 
    directory is closed.


<a href="/windows/desktop/api/fileapi/nf-fileapi-removedirectorya">RemoveDirectory</a> removes a directory junction, even 
    if the contents of the target are not empty; the function removes directory junctions regardless of the state of 
    the target object.

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
 

SMB 3.0 does not support TxF
.





> [!NOTE]
> The winbase.h header defines RemoveDirectoryTransacted as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createdirectorytransacteda">CreateDirectoryTransacted</a>



<a href="/windows/desktop/FileIO/creating-and-deleting-directories">Creating and Deleting Directories</a>



<a href="/windows/desktop/FileIO/directory-management-functions">Directory Management Functions</a>



<a href="/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>
