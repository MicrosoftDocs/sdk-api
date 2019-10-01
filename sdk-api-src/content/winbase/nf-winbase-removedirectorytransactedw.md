---
UID: NF:winbase.RemoveDirectoryTransactedW
title: RemoveDirectoryTransactedW function (winbase.h)
author: windows-sdk-content
description: Deletes an existing empty directory as a transacted operation.
old-location: fs\removedirectorytransacted.htm
tech.root: FileIO
ms.assetid: e8600166-62dc-4398-9e16-43b07f7f0b89
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RemoveDirectoryTransacted, RemoveDirectoryTransacted function [Files], RemoveDirectoryTransactedA, RemoveDirectoryTransactedW, fs.removedirectorytransacted, winbase/RemoveDirectoryTransacted, winbase/RemoveDirectoryTransactedA, winbase/RemoveDirectoryTransactedW
ms.topic: function
f1_keywords: 
 - "winbase/RemoveDirectoryTransacted"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RemoveDirectoryTransactedW function


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://docs.microsoft.com/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Deletes an existing empty directory as a transacted operation.


## -parameters




### -param lpPathName [in]

The path of the directory to be removed. The path must specify an empty directory, and the calling process 
       must have delete access to the directory.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://docs.microsoft.com/windows/desktop/FileIO/naming-a-file">Naming a File</a>.

The directory must reside on the local computer; otherwise, the function fails and the last error code is set 
       to <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.


### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
      <a href="https://docs.microsoft.com/windows/desktop/api/ktmw32/nf-ktmw32-createtransaction">CreateTransaction</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The <b>RemoveDirectoryTransacted</b> function 
    marks a directory for deletion on close. Therefore, the directory is not removed until the last handle to the 
    directory is closed.


<a href="https://docs.microsoft.com/windows/desktop/api/fileapi/nf-fileapi-removedirectorya">RemoveDirectory</a> removes a directory junction, even 
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




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createdirectorytransacteda">CreateDirectoryTransacted</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/creating-and-deleting-directories">Creating and Deleting Directories</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/directory-management-functions">Directory Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/FileIO/transactional-ntfs-portal">Transactional NTFS</a>
 

 

