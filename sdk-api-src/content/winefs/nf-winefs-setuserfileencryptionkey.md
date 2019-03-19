---
UID: NF:winefs.SetUserFileEncryptionKey
title: SetUserFileEncryptionKey function (winefs.h)
author: windows-sdk-content
description: Sets the user's current key to the specified certificate.
old-location: fs\setuserfileencryptionkey.htm
tech.root: FileIO
ms.assetid: dd23fab7-1675-4d0d-911c-e2aac2273e7f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: SetUserFileEncryptionKey, SetUserFileEncryptionKey function [Files], _win32_setuserfileencryptionkey, base.setuserfileencryptionkey, fs.setuserfileencryptionkey, winefs/SetUserFileEncryptionKey
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
 - SetUserFileEncryptionKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SetUserFileEncryptionKey function


## -description


Sets the user's current key to the specified certificate.


## -parameters




### -param pEncryptionCertificate [in]

A pointer to a certificate that will be the user's key. This parameter is a pointer to an 
<a href="https://msdn.microsoft.com/33b36659-48bb-4297-8142-f8702db03d20">ENCRYPTION_CERTIFICATE</a> structure.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is a system error code. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a> or the header file WinError.h.




## -remarks



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




<a href="https://msdn.microsoft.com/33b36659-48bb-4297-8142-f8702db03d20">ENCRYPTION_CERTIFICATE</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>
 

 

