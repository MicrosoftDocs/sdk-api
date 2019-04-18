---
UID: NF:winefs.AddUsersToEncryptedFile
title: AddUsersToEncryptedFile function (winefs.h)
author: windows-sdk-content
description: Adds user keys to the specified encrypted file.
old-location: fs\adduserstoencryptedfile.htm
tech.root: FileIO
ms.assetid: a92d6a52-20d1-4d5c-a222-ab9afaf85c4b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddUsersToEncryptedFile, AddUsersToEncryptedFile function [Files], _win32_adduserstoencryptedfile, base.adduserstoencryptedfile, fs.adduserstoencryptedfile, winefs/AddUsersToEncryptedFile
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
 - Ext-MS-Win-AdvAPI32-EncryptedFile-L1-1-1.dll
api_name:
 - AddUsersToEncryptedFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AddUsersToEncryptedFile function


## -description


Adds user keys to the specified encrypted file.


## -parameters




### -param lpFileName [in]

The name of the encrypted file.


### -param pEncryptionCertificates [in]

A pointer to an 
<a href="https://msdn.microsoft.com/e1914b96-2fba-49ed-9dd2-464659323eda">ENCRYPTION_CERTIFICATE_LIST</a> structure that contains the list of new user keys to be added to the file.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is a system error code. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a> or the header file WinError.h.




## -remarks



Starting with Windows 8 and Windows Server 2012, this function is supported by the following technologies.

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
 

SMB 3.0 does not support EFS on shares with continuous availability capability.


#### Examples

For example code that uses this function, see <a href="https://msdn.microsoft.com/39260882-dc02-4f08-9d9b-f170c1e391df">Adding Users to an Encrypted File</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e1914b96-2fba-49ed-9dd2-464659323eda">ENCRYPTION_CERTIFICATE_LIST</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>
 

 

