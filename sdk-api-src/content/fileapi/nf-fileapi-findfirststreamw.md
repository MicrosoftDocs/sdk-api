---
UID: NF:fileapi.FindFirstStreamW
title: FindFirstStreamW function
author: windows-sdk-content
description: Enumerates the first stream with a ::$DATA stream type in the specified file or directory.
old-location: fs\findfirststreamw.htm
tech.root: FileIO
ms.assetid: aab3af94-a2e0-45ad-a846-f457408a19d5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FindFirstStreamW, FindFirstStreamW function [Files], FindStreamInfoStandard, _win32_findfirststreamw, base.findfirststreamw, fileapi/FindFirstStreamW, fs.findfirststreamw
ms.topic: function
req.header: fileapi.h
req.include-header: Windows.h, WinBase.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - API-MS-Win-Core-File-l1-2-2.dll
 - KernelBase.dll
 - MinKernelBase.dll
api_name:
 - FindFirstStreamW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FindFirstStreamW function


## -description


Enumerates the first stream with a ::$DATA stream type in the specified file or 
    directory.

To perform this operation as a transacted operation, use the 
    <a href="https://msdn.microsoft.com/76c64aa9-0501-457d-b774-c209fbac4ccc">FindFirstStreamTransactedW</a> 
    function.


## -parameters




### -param lpFileName [in]

The fully qualified file name.


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

A pointer to a buffer that receives the file stream data. The format of this data depends on the value of 
      the <i>InfoLevel</i> parameter.


### -param dwFlags

Reserved for future use. This parameter must be zero.


## -returns



If the function succeeds, the return value is a search handle that can be used in subsequent calls to the 
       <a href="https://msdn.microsoft.com/2bb0301c-b2be-4056-913c-e4102386135e">FindNextStreamW</a> function.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended 
       error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

If no  streams can be found, the function fails and 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
       <b>ERROR_HANDLE_EOF</b> (38).




## -remarks



The <b>FindFirstStreamW</b> function opens a search 
    handle and returns information about the first ::$DATA stream in the specified file or directory. For 
    files, this is always the default data stream, "::$DATA". After the search handle has been 
    established, use it in the <a href="https://msdn.microsoft.com/2bb0301c-b2be-4056-913c-e4102386135e">FindNextStreamW</a> function to 
    search for other streams in the specified file or directory. When the search handle is no longer needed, it should 
    be closed using the <a href="https://msdn.microsoft.com/64b3bc49-1e0e-4572-9d9f-936c45f5b01c">FindClose</a> function.

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
 

SMB 3.0 supports list of streams less than or equal to 64K.




## -see-also




<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/64b3bc49-1e0e-4572-9d9f-936c45f5b01c">FindClose</a>



<a href="https://msdn.microsoft.com/76c64aa9-0501-457d-b774-c209fbac4ccc">FindFirstStreamTransactedW</a>



<a href="https://msdn.microsoft.com/2bb0301c-b2be-4056-913c-e4102386135e">FindNextStreamW</a>



<a href="https://msdn.microsoft.com/411efcdc-e13a-4f27-a3da-31dff714e415">STREAM_INFO_LEVELS</a>



<a href="https://msdn.microsoft.com/f21f5161-10a8-474c-85d8-dde075b9daff">WIN32_FIND_STREAM_DATA</a>
 

 

