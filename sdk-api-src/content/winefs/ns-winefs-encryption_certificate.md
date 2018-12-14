---
UID: NS:winefs._ENCRYPTION_CERTIFICATE
title: ENCRYPTION_CERTIFICATE
author: windows-sdk-content
description: Contains a certificate and the SID of its owner.
old-location: fs\encryption_certificate_str.htm
tech.root: fileio
ms.assetid: 33b36659-48bb-4297-8142-f8702db03d20
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PENCRYPTION_CERTIFICATE, ENCRYPTION_CERTIFICATE, ENCRYPTION_CERTIFICATE structure [Files], PENCRYPTION_CERTIFICATE, PENCRYPTION_CERTIFICATE structure pointer [Files], _win32_encryption_certificate_str, base.encryption_certificate_str, fs.encryption_certificate_str, winefs/ENCRYPTION_CERTIFICATE, winefs/PENCRYPTION_CERTIFICATE"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winefs.h
api_name:
 - ENCRYPTION_CERTIFICATE
product: Windows
targetos: Windows
req.typenames: ENCRYPTION_CERTIFICATE, *PENCRYPTION_CERTIFICATE
req.redist: 
---

# ENCRYPTION_CERTIFICATE structure


## -description


Contains a certificate and the SID of its owner.


## -struct-fields




### -field cbTotalLength

The length of this structure, in bytes.


### -field pUserSid

The <a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> of the user who owns the certificate.


### -field pCertBlob

A pointer to an 
<a href="https://msdn.microsoft.com/e0d0aa0a-ac87-4734-93d0-30c2080319e8">EFS_CERTIFICATE_BLOB</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/e0d0aa0a-ac87-4734-93d0-30c2080319e8">EFS_CERTIFICATE_BLOB</a>



<a href="https://msdn.microsoft.com/e1914b96-2fba-49ed-9dd2-464659323eda">ENCRYPTION_CERTIFICATE_LIST</a>



<a href="https://msdn.microsoft.com/5f20109f-727d-44a9-90a1-0adc19b00d28">File Encryption</a>



<a href="https://msdn.microsoft.com/dd23fab7-1675-4d0d-911c-e2aac2273e7f">SetUserFileEncryptionKey</a>
 

 

