---
UID: NF:winbase.GetFullPathNameTransactedW
title: GetFullPathNameTransactedW function
author: windows-sdk-content
description: Retrieves the full path and file name of the specified file as a transacted operation.
old-location: fs\getfullpathnametransacted.htm
old-project: fileio
ms.assetid: 63cbcec6-e9f0-4db3-bf2f-03a987000af1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetFullPathNameTransacted, GetFullPathNameTransacted function [Files], GetFullPathNameTransactedA, GetFullPathNameTransactedW, fs.getfullpathnametransacted, winbase/GetFullPathNameTransacted, winbase/GetFullPathNameTransactedA, winbase/GetFullPathNameTransactedW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetFullPathNameTransactedW (Unicode) and GetFullPathNameTransactedA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - Kernel32Legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - GetFullPathNameTransacted
 - GetFullPathNameTransactedA
 - GetFullPathNameTransactedW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# GetFullPathNameTransactedW function


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Retrieves the full path and file name of the specified file as a transacted operation.

To perform this operation without transactions, use the 
    <a href="https://msdn.microsoft.com/4cf59ee3-4065-4096-a2b5-fbed20aa5caa">GetFullPathName</a> function.

For more information about file and path names, see 
    <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">File Names, Paths, and Namespaces</a>.


## -parameters




### -param lpFileName [in]

The name of the file.

This string can use short (the 8.3 form) or long file names. This string can be a share or volume name.

The file must reside on the local computer; otherwise, the function fails and the last error code is set to 
       <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.


### -param nBufferLength [in]

The size of the buffer to receive the null-terminated string  for the drive and path,  in 
      <b>TCHARs</b>.


### -param lpBuffer [out]

A pointer to a buffer that receives the null-terminated string for the  drive and path.


### -param lpFilePart [out]

A pointer to a buffer that receives the address (in <i>lpBuffer</i>) of the final file 
       name component in the path. Specify <b>NULL</b> if you do not need to receive this 
       information.

If <i>lpBuffer</i> points to a directory and not a file, 
       <i>lpFilePart</i> receives 0 (zero).


### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
      <a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a> function.


## -returns



If the function succeeds, the return value is the length, in <b>TCHARs</b>, of the 
       string copied to <i>lpBuffer</i>, not including the terminating null character.

If the <i>lpBuffer</i> buffer is too small to contain the path, the return value is the 
       size, in <b>TCHARs</b>, of the buffer that is required to hold the path and the 
       terminating null character.

If the function fails for any other reason, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



<b>GetFullPathNameTransacted</b> merges the name 
    of the current drive and directory with a specified file name to determine the full path and file name of a 
    specified file. It also calculates the address of the file name portion of the full path and file name. This 
    function does not verify that the resulting path and file name are valid, or that they see an existing file on the 
    associated volume.

Share and volume names are valid input for <i>lpFileName</i>. For example, the following 
    list identities the returned path and file names if test-2 is a remote computer and U: is a network mapped drive:

<ul>
<li>If you specify "\\test-2\q$\lh" the path returned is 
      "\\test-2\q$\lh"</li>
<li>If you specify "\\?\UNC\test-2\q$\lh" the path returned is 
      "\\?\UNC\test-2\q$\lh"</li>
<li>If you specify "U:" the path returned is "U:\"</li>
</ul>
<b>GetFullPathNameTransacted</b> does not convert 
    the specified file name, <i>lpFileName</i>. If the specified file name exists, you can use 
    <a href="https://msdn.microsoft.com/8523cde9-f0dd-4832-8d9d-9e68bac89344">GetLongPathNameTransacted</a>, 
    <a href="https://msdn.microsoft.com/8ce69033-b69b-438b-a27f-938dd327c8ec">GetLongPathName</a>, or 
    <a href="https://msdn.microsoft.com/15c794d6-6d6b-4ee0-b5b7-a2cf6f5ec5e7">GetShortPathName</a> to convert to long or short path 
    names, respectively.

If the return value is greater than the value specified in <i>nBufferLength</i>, you can 
    call the function again with a buffer that is large enough to hold the path. For an example of this case as well 
    as using zero length buffer for dynamic allocation, see the Example Code section.

<div class="alert"><b>Note</b>  Although the return value in this case is a length that includes the terminating null character, the return 
     value on success does not include the terminating null character in the count.</div>
<div> </div>
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




## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/4cf59ee3-4065-4096-a2b5-fbed20aa5caa">GetFullPathName</a>



<a href="https://msdn.microsoft.com/8523cde9-f0dd-4832-8d9d-9e68bac89344">GetLongPathNameTransacted</a>



<a href="https://msdn.microsoft.com/15c794d6-6d6b-4ee0-b5b7-a2cf6f5ec5e7">GetShortPathName</a>



<a href="https://msdn.microsoft.com/fb366f0d-df6b-44c2-92c9-b7a8e2583054">GetTempPath</a>



<a href="https://msdn.microsoft.com/8039365a-1b39-431e-af87-9a9933ca102d">SearchPath</a>



<a href="https://msdn.microsoft.com/e8c3ceed-d391-4934-b3f7-12c2123c8c23">Transactional NTFS</a>
 

 

