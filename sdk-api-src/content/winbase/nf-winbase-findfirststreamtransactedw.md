---
UID: NF:winbase.FindFirstStreamTransactedW
title: FindFirstStreamTransactedW function
author: windows-sdk-content
description: Enumerates the first stream in the specified file or directory as a transacted operation.
old-location: fs\findfirststreamtransactedw.htm
tech.root: FileIO
ms.assetid: 76c64aa9-0501-457d-b774-c209fbac4ccc
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: FindFirstStreamTransactedW, FindFirstStreamTransactedW function [Files], FindStreamInfoStandard, fs.findfirststreamtransactedw, winbase/FindFirstStreamTransactedW
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
req.unicode-ansi: 
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
api_name:
 - FindFirstStreamTransactedW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FindFirstStreamTransactedW function


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Enumerates the first stream in the specified file or directory as a transacted 
    operation.


## -parameters




### -param lpFileName [in]

The fully qualified file name.

The file must reside on the local computer; otherwise, the function fails and the last error code is set to 
       <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b> (6805).


### -param InfoLevel [in]

The information level of the returned data. This parameter is one of the values in the 
      <a href="https://msdn.microsoft.com/411efcdc-e13a-4f27-a3da-31dff714e415">STREAM_INFO_LEVELS</a> enumeration type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FindStreamInfoStandard"></a><a id="findstreaminfostandard"></a><a id="FINDSTREAMINFOSTANDARD"></a><dl>
<dt><b>FindStreamInfoStandard</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The data is returned in a 
        <a href="https://msdn.microsoft.com/f21f5161-10a8-474c-85d8-dde075b9daff">WIN32_FIND_STREAM_DATA</a> structure.

</td>
</tr>
</table>
 


### -param lpFindStreamData [out]

A pointer to a buffer that receives the file data. The format of this data depends on the value of 
       the <i>InfoLevel</i> parameter.


### -param dwFlags

Reserved for future use. This parameter must be zero.


### -param hTransaction [in]

A handle to the transaction. This handle is returned by the 
       <a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a> function.


## -returns



If the function succeeds, the return value is a search handle that can be used in subsequent calls to the 
       <a href="https://msdn.microsoft.com/2bb0301c-b2be-4056-913c-e4102386135e">FindNextStreamW</a>function.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended 
       error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



All files contain a default data stream. On NTFS, files can also contain one or more named data streams. On 
    FAT file systems, files cannot have more that the default data stream, and therefore, this function will not 
    return valid results when used on FAT filesystem files. This function works on all file systems that supports hard 
    links; otherwise, the function returns <b>ERROR_STATUS_NOT_IMPLEMENTED</b> (6805).

The <b>FindFirstStreamTransactedW</b> function 
    opens a search handle and returns information about the first stream in the specified file or directory. For 
    files, this is always the default data stream, ::$DATA. After the search handle has been established, use it in 
    the <a href="https://msdn.microsoft.com/2bb0301c-b2be-4056-913c-e4102386135e">FindNextStreamW</a> function to search for other 
    streams in the specified file or directory. When the search handle is no longer needed, it should be closed using 
    the <a href="https://msdn.microsoft.com/64b3bc49-1e0e-4572-9d9f-936c45f5b01c">FindClose</a>function.

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



<a href="https://msdn.microsoft.com/64b3bc49-1e0e-4572-9d9f-936c45f5b01c">FindClose</a>



<a href="https://msdn.microsoft.com/2bb0301c-b2be-4056-913c-e4102386135e">FindNextStreamW</a>



<a href="https://msdn.microsoft.com/411efcdc-e13a-4f27-a3da-31dff714e415">STREAM_INFO_LEVELS</a>



<a href="https://msdn.microsoft.com/e8c3ceed-d391-4934-b3f7-12c2123c8c23">Transactional NTFS</a>



<a href="https://msdn.microsoft.com/f21f5161-10a8-474c-85d8-dde075b9daff">WIN32_FIND_STREAM_DATA</a>
 

 

