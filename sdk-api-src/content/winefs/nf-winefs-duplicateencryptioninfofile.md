---
UID: NF:winefs.DuplicateEncryptionInfoFile
title: DuplicateEncryptionInfoFile function (winefs.h)
author: windows-sdk-content
description: Copies the EFS metadata from one file or directory to another.
old-location: fs\duplicateencryptioninfofile.htm
tech.root: FileIO
ms.assetid: c830ae98-3649-4981-9369-7d4cb019b50f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CREATE_ALWAYS, CREATE_NEW, DuplicateEncryptionInfoFile, DuplicateEncryptionInfoFile function [Files], _win32_duplicateencryptioninfofile, base.duplicateencryptioninfofile, fs.duplicateencryptioninfofile, winefs/DuplicateEncryptionInfoFile
ms.topic: function
req.header: winefs.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP Professional [desktop apps only]
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - DuplicateEncryptionInfoFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DuplicateEncryptionInfoFile function


## -description


Copies the EFS metadata from one file or directory to another.


## -parameters




### -param SrcFileName [in]

The name of the file or directory from which the EFS metadata is to be copied. This source file or directory must be encrypted.


### -param DstFileName [in]

The name of the file or directory to which the EFS metadata is to be copied. 




This destination file or directory does not have to be encrypted before the call to this function; however if this function completes successfully, it will be encrypted.

If the value of <i>SrcFileName</i> specifies a file, the value of this parameter must also specify a file, and likewise for directories. If a file or directory with the name specified by this parameter does not exist, a file or directory (depending on whether <i>SrcFileName</i> specifies a file or directory) will be created.


### -param dwCreationDistribution [in]

Describes how the destination file or directory identified by the <i>DstFileName</i> parameter value is to be opened. The following are the valid values of this parameter. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREATE_ALWAYS"></a><a id="create_always"></a><dl>
<dt><b>CREATE_ALWAYS</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Always create the destination file or directory. Any value passed in this parameter other than <b>CREATE_NEW</b> will be processed as <b>CREATE_ALWAYS</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_NEW"></a><a id="create_new"></a><dl>
<dt><b>CREATE_NEW</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Create the destination file or directory only if it does not already exist. If it does exist, and this value is specified, this function will fail.

</td>
</tr>
</table>
 


### -param dwAttributes [in]

The file attributes of the destination file or directory. The <b>FILE_READ_ONLY</b> attribute is currently not processed by this function.


### -param lpSecurityAttributes [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure that specifies the security attributes of the destination file or directory, if it does not already exist. If you specify <b>NULL</b>, the file or directory gets a default security descriptor. The ACLs in the default security descriptor for a file or directory are inherited from its parent directory.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is a system error code. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a> or the header file WinError.h.




## -remarks



Exclusive access to the destination file or directory is required by EFS for the call to this function. If this access is not provided, this function will fail.

The caller should have the EFS key for the source file or directory, and at least the <b>READ_ATTRIBUTE</b> ACL for the source file or directory.

The specified source and destination file or directories should reside on the same computer; otherwise, an error will be returned.

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
 

SMB 3.0 does not support EFS on shares with continuous availability capability.





## -see-also




<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>
 

 

