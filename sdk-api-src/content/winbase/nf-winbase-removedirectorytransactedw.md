---
UID: NF:winbase.RemoveDirectoryTransactedW
title: RemoveDirectoryTransactedW function
author: windows-driver-content
description: Deletes an existing empty directory as a transacted operation.
old-location: fs\removedirectorytransacted.htm
old-project: FileIO
ms.assetid: e8600166-62dc-4398-9e16-43b07f7f0b89
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: RemoveDirectoryTransacted, RemoveDirectoryTransacted function [Files], RemoveDirectoryTransactedA, RemoveDirectoryTransactedW, fs.removedirectorytransacted, winbase/RemoveDirectoryTransacted, winbase/RemoveDirectoryTransactedA, winbase/RemoveDirectoryTransactedW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	Ext-MS-Win-Kernel32-Transacted-l1-1-0.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
-	Kernel32Legacy.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
-	RemoveDirectoryTransacted
-	RemoveDirectoryTransactedA
-	RemoveDirectoryTransactedW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# RemoveDirectoryTransactedW function


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Deletes an existing empty directory as a transacted operation.


## -parameters




### -param lpPathName [in]

The path of the directory to be removed. The path must specify an empty directory, and the calling process 
       must have delete access to the directory.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

The directory must reside on the local computer; otherwise, the function fails and the last error code is set 
       to <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.


### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
      <a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>RemoveDirectoryTransacted</b> function 
    marks a directory for deletion on close. Therefore, the directory is not removed until the last handle to the 
    directory is closed.


<a href="https://msdn.microsoft.com/d699cdd2-e270-4f17-bdec-6eea25b01578">RemoveDirectory</a> removes a directory junction, even 
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




<a href="https://msdn.microsoft.com/75663b30-5bd9-4de7-8e4f-dc58016c2c40">CreateDirectoryTransacted</a>



<a href="https://msdn.microsoft.com/52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32">Creating and Deleting Directories</a>



<a href="https://msdn.microsoft.com/5517b0e7-2264-4173-8e10-ff7626458bfa">Directory Management Functions</a>



<a href="https://msdn.microsoft.com/e8c3ceed-d391-4934-b3f7-12c2123c8c23">Transactional NTFS</a>
 

 

