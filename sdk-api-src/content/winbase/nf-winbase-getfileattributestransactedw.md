---
UID: NF:winbase.GetFileAttributesTransactedW
title: GetFileAttributesTransactedW function
author: windows-sdk-content
description: Retrieves file system attributes for a specified file or directory as a transacted operation.
old-location: fs\getfileattributestransacted.htm
tech.root: fileio
ms.assetid: dd1435da-93e5-440a-913a-9e40e39b4a01
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetFileAttributesTransacted, GetFileAttributesTransacted function [Files], GetFileAttributesTransactedA, GetFileAttributesTransactedW, GetFileExInfoStandard, fs.getfileattributestransacted, winbase/GetFileAttributesTransacted, winbase/GetFileAttributesTransactedA, winbase/GetFileAttributesTransactedW
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
req.unicode-ansi: GetFileAttributesTransactedW (Unicode) and GetFileAttributesTransactedA (ANSI)
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetFileAttributesTransactedW function


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Retrieves file system attributes for a specified file or directory as a transacted 
    operation.


## -parameters




### -param lpFileName [in]

The name of the file or directory.
      

In the ANSI version of this function, the name is limited to <b>MAX_PATH</b> characters. 
       To extend this limit to 32,767 wide characters, call the Unicode version of the function and prepend 
       "\\?\" to the path. For more information, see 
       <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

The file or directory must reside on the local computer; otherwise, the function fails and the last error code is set to <b>ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE</b>.


### -param fInfoLevelId [in]

The level of attribute information to retrieve.
      

This parameter can be the following value from the 
       <a href="https://msdn.microsoft.com/1004ab99-9c08-4ed4-ba5f-d72f1b44a415">GET_FILEEX_INFO_LEVELS</a> enumeration.

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
        <a href="https://msdn.microsoft.com/e1a7fb5c-2d69-40e3-b9d8-b583a03d828a">WIN32_FILE_ATTRIBUTE_DATA</a> 
        structure.

</td>
</tr>
</table>
 


### -param lpFileInformation [out]

A pointer to a buffer that receives the attribute information.
      

The type of attribute information that is stored into this buffer is determined by the value of 
       <i>fInfoLevelId</i>. If the <i>fInfoLevelId</i> parameter is 
       <b>GetFileExInfoStandard</b> then this parameter points to a 
       <a href="https://msdn.microsoft.com/e1a7fb5c-2d69-40e3-b9d8-b583a03d828a">WIN32_FILE_ATTRIBUTE_DATA</a> 
        structure


### -param hTransaction [in]

A handle to the transaction. This handle is returned by the <a href="https://msdn.microsoft.com/578bda35-bd35-4f6d-8366-a4bfb4dbfe42">CreateTransaction</a> function.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended 
       error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When <b>GetFileAttributesTransacted</b> is 
    called on a directory that is a mounted folder, it returns the attributes of the directory, not those of the root directory in the volume that the mounted folder associates with the directory. To obtain the 
    file attributes of the associated volume, call 
    <a href="https://msdn.microsoft.com/3f749042-bdc9-4087-bb8a-d833713472eb">GetVolumeNameForVolumeMountPoint</a> to 
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




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156">File Attribute Constants</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/d94bf32b-f14b-44b4-824b-ed453d0424ef">FindFirstFileTransacted</a>



<a href="https://msdn.microsoft.com/db7acb83-2da6-40bf-9962-5cfe54e257a5">FindNextFile</a>



<a href="https://msdn.microsoft.com/1004ab99-9c08-4ed4-ba5f-d72f1b44a415">GET_FILEEX_INFO_LEVELS</a>



<a href="https://msdn.microsoft.com/e25e77b2-a6ad-4ce4-8589-d7ff6c4074f6">SetFileAttributesTransacted</a>



<a href="https://msdn.microsoft.com/d6bf5df7-bc12-4dec-b116-95d9109f5eb4">Symbolic Links</a>



<a href="https://msdn.microsoft.com/e8c3ceed-d391-4934-b3f7-12c2123c8c23">Transactional NTFS</a>
 

 

