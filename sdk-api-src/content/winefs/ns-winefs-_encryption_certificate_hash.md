---
UID: NS:winefs._ENCRYPTION_CERTIFICATE_HASH
title: "_ENCRYPTION_CERTIFICATE_HASH"
author: windows-sdk-content
description: Contains a certificate hash and display information for the certificate.
old-location: fs\encryption_certificate_hash_str.htm
tech.root: fileio
ms.assetid: 6930446c-5338-4ff9-a662-791fc9e7cefe
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PENCRYPTION_CERTIFICATE_HASH, ENCRYPTION_CERTIFICATE_HASH, ENCRYPTION_CERTIFICATE_HASH structure [Files], PENCRYPTION_CERTIFICATE_HASH, PENCRYPTION_CERTIFICATE_HASH structure pointer [Files], _ENCRYPTION_CERTIFICATE_HASH, _win32_encryption_certificate_hash_str, base.encryption_certificate_hash_str, fs.encryption_certificate_hash_str, winefs/ENCRYPTION_CERTIFICATE_HASH, winefs/PENCRYPTION_CERTIFICATE_HASH"
ms.prod: windows
ms.technology: windows-sdk
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
 - ENCRYPTION_CERTIFICATE_HASH
product: Windows
targetos: Windows
req.typenames: ENCRYPTION_CERTIFICATE_HASH, *PENCRYPTION_CERTIFICATE_HASH
req.redist: 
---

# _ENCRYPTION_CERTIFICATE_HASH structure


## -description


Contains a certificate hash and display information for the certificate.


## -struct-fields




### -field cbTotalLength

The length of this structure, in bytes.


### -field pUserSid

The <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> of the user who created the certificate. This member is optional and can be <b>NULL</b>.


### -field pHash

A pointer to an 
<a href="https://msdn.microsoft.com/23a172be-6e94-4a1f-afde-fc9437443c7a">EFS_HASH_BLOB</a> structure.


### -field lpDisplayInformation

User-displayable information for the certificate.  This is usually the user's common name and universal principal name (UPN).


### -field lpDisplayInformation.string

 




## -see-also




<a href="https://msdn.microsoft.com/23a172be-6e94-4a1f-afde-fc9437443c7a">EFS_HASH_BLOB</a>



<a href="https://msdn.microsoft.com/988159b3-3cb9-4a4d-9c68-ebfb309cff25">ENCRYPTION_CERTIFICATE_HASH_LIST</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>
 

 

