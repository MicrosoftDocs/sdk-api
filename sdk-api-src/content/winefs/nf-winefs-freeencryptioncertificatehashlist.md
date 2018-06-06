---
UID: NF:winefs.FreeEncryptionCertificateHashList
title: FreeEncryptionCertificateHashList function
author: windows-sdk-content
description: Frees a certificate hash list.
old-location: fs\freeencryptioncertificatehashlist.htm
old-project: FileIO
ms.assetid: 63d5811f-a135-45b0-8f23-fd8851f7bcca
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: FreeEncryptionCertificateHashList, FreeEncryptionCertificateHashList function [Files], _win32_freeencryptioncertificatehashlist, base.freeencryptioncertificatehashlist, fs.freeencryptioncertificatehashlist, winefs/FreeEncryptionCertificateHashList
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: HANDLE_SHARING_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - Ext-MS-Win-AdvAPI32-EncryptedFile-l1-1-0.dll
 - Ext-MS-Win-AdvAPI32-EncryptedFile-L1-1-1.dll
api_name:
 - FreeEncryptionCertificateHashList
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# FreeEncryptionCertificateHashList function


## -description


Frees a certificate hash list.


## -parameters




### -param pUsers

TBD




#### - pHashes [in]

A pointer to a certificate hash list structure, 
<a href="https://msdn.microsoft.com/988159b3-3cb9-4a4d-9c68-ebfb309cff25">ENCRYPTION_CERTIFICATE_HASH_LIST</a>, which was returned by the 
<a href="https://msdn.microsoft.com/1bdab753-e7f2-4c08-8b37-3903c0842227">QueryUsersOnEncryptedFile</a> or 
<a href="https://msdn.microsoft.com/2f8d0673-3c87-46a4-b7d5-3888d20bd9b8">QueryRecoveryAgentsOnEncryptedFile</a> function.


## -returns



This function does not return a value.




## -remarks



<b>ReFS:  </b>This function is not supported.




## -see-also




<a href="https://msdn.microsoft.com/988159b3-3cb9-4a4d-9c68-ebfb309cff25">ENCRYPTION_CERTIFICATE_HASH_LIST</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/2f8d0673-3c87-46a4-b7d5-3888d20bd9b8">QueryRecoveryAgentsOnEncryptedFile</a>



<a href="https://msdn.microsoft.com/1bdab753-e7f2-4c08-8b37-3903c0842227">QueryUsersOnEncryptedFile</a>
 

 

