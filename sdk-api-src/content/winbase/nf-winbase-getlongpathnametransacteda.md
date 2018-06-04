---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# GetLongPathNameTransactedA function


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Converts the specified path to its long form as a transacted operation.

To perform this operation without a transaction, use the 
    <a href="https://msdn.microsoft.com/8ce69033-b69b-438b-a27f-938dd327c8ec">GetLongPathName</a> function.

For more information about file and path names, see 
    <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a>.


## -parameters




### -param lpszShortPath [in]

The path to be converted.

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> (260) 
       characters. To extend this limit to 32,767 wide characters, call the Unicode version of the function and 
       prepend "\\?\" to the path. For more information, see 
      <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a>.

The path must reside on the local computer; otherwise, the function fails and the last error code is set to 
      <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.


### -param lpszLongPath [out]

A pointer to the buffer to receive the long path.

You can use the same buffer you used for the <i>lpszShortPath</i> parameter.


### -param cchBuffer [in]

The size of the buffer <i>lpszLongPath</i> points to, in 
      <b>TCHAR</b>s.


### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
      <a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a> function.


## -returns



If the function succeeds, the return value is the length, in <b>TCHAR</b>s, of the 
       string copied to <i>lpszLongPath</i>, not including the terminating null character.

If the <i>lpBuffer</i> buffer is too small to contain the path, the return value is the 
       size, in <b>TCHAR</b>s, of the buffer that is required to hold the path and the 
       terminating null character.

If the function fails for any other reason, such as if the file does not exist, the return value is zero. To 
       get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



On many file systems, a short file name contains a tilde (~) character. However, not all file systems follow 
    this convention. Therefore, do not assume that you can skip calling 
    <b>GetLongPathNameTransacted</b> if the path does not 
    contain a tilde (~) character.

If a long path is not found, this function returns the name specified in the 
    <i>lpszShortPath</i> parameter in the <i>lpszLongPath</i> parameter.

If the return value is greater than the value specified in <i>cchBuffer</i>, you can call 
    the function again with a buffer that is large enough to hold the path. For an example of this case, see the 
    Example Code section for <a href="https://msdn.microsoft.com/4cf59ee3-4065-4096-a2b5-fbed20aa5caa">GetFullPathName</a>.

<div class="alert"><b>Note</b>  Although the return value in this case is a length that includes the terminating null character, the return 
     value on success does not include the terminating null character in the count.</div>
<div> </div>
It is possible to have access to a file or directory but not have access to some of the parent directories of 
    that file or directory. As a result, 
    <b>GetLongPathNameTransacted</b> may fail when it is 
    unable to query the parent directory of a path component to determine the long name for that component. This check 
    can be skipped for directory components that have file extensions longer than 3 characters, or total lengths 
    longer than 12 characters. For more information, see the 
    <a href="naming_a_file.htm">Short vs. Long Names</a> section of 
    <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a>.

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



<a href="https://msdn.microsoft.com/63cbcec6-e9f0-4db3-bf2f-03a987000af1">GetFullPathNameTransacted</a>



<a href="https://msdn.microsoft.com/15c794d6-6d6b-4ee0-b5b7-a2cf6f5ec5e7">GetShortPathName</a>



<a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a>



<a href="https://msdn.microsoft.com/e8c3ceed-d391-4934-b3f7-12c2123c8c23">Transactional NTFS</a>
 

 

