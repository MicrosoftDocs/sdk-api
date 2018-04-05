---
UID: NF:winefs.QueryRecoveryAgentsOnEncryptedFile
title: QueryRecoveryAgentsOnEncryptedFile function
author: windows-driver-content
description: Retrieves a list of recovery agents for the specified file.
old-location: fs\queryrecoveryagentsonencryptedfile.htm
old-project: FileIO
ms.assetid: 2f8d0673-3c87-46a4-b7d5-3888d20bd9b8
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: QueryRecoveryAgentsOnEncryptedFile, QueryRecoveryAgentsOnEncryptedFile function [Files], _win32_queryrecoveryagentsonencryptedfile, base.queryrecoveryagentsonencryptedfile, fs.queryrecoveryagentsonencryptedfile, winefs/QueryRecoveryAgentsOnEncryptedFile
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
-	Ext-MS-Win-AdvAPI32-EncryptedFile-L1-1-1.dll
api_name:
-	QueryRecoveryAgentsOnEncryptedFile
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# QueryRecoveryAgentsOnEncryptedFile function


## -description


Retrieves a list of recovery agents for the specified file.


## -parameters




### -param lpFileName [in]

The name of the file.


### -param pRecoveryAgents [out]

A pointer to a 
<a href="https://msdn.microsoft.com/988159b3-3cb9-4a4d-9c68-ebfb309cff25">ENCRYPTION_CERTIFICATE_HASH_LIST</a> structure that receives a list of recovery agents.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is a system error code. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a> or the header file WinError.h.




## -remarks



When the list of recovery agents is no longer needed, free it by calling the 
<a href="https://msdn.microsoft.com/63d5811f-a135-45b0-8f23-fd8851f7bcca">FreeEncryptionCertificateHashList</a> function.

In Windows 8, Windows Server 2012, and later, this function is supported by the following technologies.

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




<a href="https://msdn.microsoft.com/988159b3-3cb9-4a4d-9c68-ebfb309cff25">ENCRYPTION_CERTIFICATE_HASH_LIST</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/63d5811f-a135-45b0-8f23-fd8851f7bcca">FreeEncryptionCertificateHashList</a>
 

 

