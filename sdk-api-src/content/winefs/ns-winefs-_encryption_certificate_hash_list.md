---
UID: NS:winefs._ENCRYPTION_CERTIFICATE_HASH_LIST
title: "_ENCRYPTION_CERTIFICATE_HASH_LIST"
author: windows-sdk-content
description: Contains a list of certificate hashes.
old-location: fs\encryption_certificate_hash_list_str.htm
tech.root: fileio
ms.assetid: 988159b3-3cb9-4a4d-9c68-ebfb309cff25
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PENCRYPTION_CERTIFICATE_HASH_LIST, ENCRYPTION_CERTIFICATE_HASH_LIST, ENCRYPTION_CERTIFICATE_HASH_LIST structure [Files], PENCRYPTION_CERTIFICATE_HASH_LIST, PENCRYPTION_CERTIFICATE_HASH_LIST structure pointer [Files], _ENCRYPTION_CERTIFICATE_HASH_LIST, _win32_encryption_certificate_hash_list_str, base.encryption_certificate_hash_list_str, fs.encryption_certificate_hash_list_str, winefs/ENCRYPTION_CERTIFICATE_HASH_LIST, winefs/PENCRYPTION_CERTIFICATE_HASH_LIST"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winefs.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEfs.h
api_name:
 - ENCRYPTION_CERTIFICATE_HASH_LIST
product: Windows
targetos: Windows
req.typenames: ENCRYPTION_CERTIFICATE_HASH_LIST, *PENCRYPTION_CERTIFICATE_HASH_LIST
req.redist: 
---

# _ENCRYPTION_CERTIFICATE_HASH_LIST structure


## -description


Contains a list of certificate hashes.


## -struct-fields




### -field nCert_Hash

The number of certificate hashes in the list.


### -field nCert_Hash.range

 


### -field nCert_Hash.range.0

 


### -field nCert_Hash.range.500

 


### -field pUsers

A pointer to the first 
<a href="https://msdn.microsoft.com/6930446c-5338-4ff9-a662-791fc9e7cefe">ENCRYPTION_CERTIFICATE_HASH</a> structure in the list. 


### -field pUsers.size_is

 


### -field pUsers.size_is.nCert_Hash

 




## -see-also




<a href="https://msdn.microsoft.com/6930446c-5338-4ff9-a662-791fc9e7cefe">ENCRYPTION_CERTIFICATE_HASH</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>



<a href="https://msdn.microsoft.com/63d5811f-a135-45b0-8f23-fd8851f7bcca">FreeEncryptionCertificateHashList</a>



<a href="https://msdn.microsoft.com/2f8d0673-3c87-46a4-b7d5-3888d20bd9b8">QueryRecoveryAgentsOnEncryptedFile</a>



<a href="https://msdn.microsoft.com/1bdab753-e7f2-4c08-8b37-3903c0842227">QueryUsersOnEncryptedFile</a>



<a href="https://msdn.microsoft.com/c6672581-24b4-464c-b32d-48a04e56eef8">RemoveUsersFromEncryptedFile</a>
 

 

