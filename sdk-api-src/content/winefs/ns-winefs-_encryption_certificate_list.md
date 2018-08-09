---
UID: NS:winefs._ENCRYPTION_CERTIFICATE_LIST
title: "_ENCRYPTION_CERTIFICATE_LIST"
author: windows-sdk-content
description: Contains a list of certificates.
old-location: fs\encryption_certificate_list_str.htm
old-project: fileio
ms.assetid: e1914b96-2fba-49ed-9dd2-464659323eda
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PENCRYPTION_CERTIFICATE_LIST, ENCRYPTION_CERTIFICATE_LIST, ENCRYPTION_CERTIFICATE_LIST structure [Files], PENCRYPTION_CERTIFICATE_LIST, PENCRYPTION_CERTIFICATE_LIST structure pointer [Files], _ENCRYPTION_CERTIFICATE_LIST, _win32_encryption_certificate_list_str, base.encryption_certificate_list_str, fs.encryption_certificate_list_str, winefs/ENCRYPTION_CERTIFICATE_LIST, winefs/PENCRYPTION_CERTIFICATE_LIST"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: ENCRYPTION_CERTIFICATE_LIST, *PENCRYPTION_CERTIFICATE_LIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinEfs.h
api_name:
 - ENCRYPTION_CERTIFICATE_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _ENCRYPTION_CERTIFICATE_LIST structure


## -description


Contains a list of certificates.


## -struct-fields




### -field nUsers

The number of certificates in the list.


### -field nUsers.range

 


### -field nUsers.range.0

 


### -field nUsers.range.500

 


### -field pUsers

A pointer to the first 
						<a href="https://msdn.microsoft.com/33b36659-48bb-4297-8142-f8702db03d20">ENCRYPTION_CERTIFICATE</a> structure in the list.


### -field pUsers.size_is

 


### -field pUsers.size_is.nUsers

 




## -see-also




<a href="https://msdn.microsoft.com/a92d6a52-20d1-4d5c-a222-ab9afaf85c4b">AddUsersToEncryptedFile</a>



<a href="https://msdn.microsoft.com/33b36659-48bb-4297-8142-f8702db03d20">ENCRYPTION_CERTIFICATE</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>
 

 

