---
UID: NS:wincrypt._CERT_PRIVATE_KEY_VALIDITY
title: "_CERT_PRIVATE_KEY_VALIDITY"
author: windows-sdk-content
description: The CERT_PRIVATE_KEY_VALIDITY structure indicates a valid time span for the private key corresponding to a certificate's public key.
old-location: security\cert_private_key_validity.htm
old-project: SecCrypto
ms.assetid: 4764174f-eecc-402e-8395-d3e2be0b0ae6
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*PCERT_PRIVATE_KEY_VALIDITY, CERT_PRIVATE_KEY_VALIDITY, CERT_PRIVATE_KEY_VALIDITY structure [Security], PCERT_PRIVATE_KEY_VALIDITY, PCERT_PRIVATE_KEY_VALIDITY structure pointer [Security], _CERT_PRIVATE_KEY_VALIDITY, _crypto2_cert_private_key_validity, security.cert_private_key_validity, wincrypt/CERT_PRIVATE_KEY_VALIDITY, wincrypt/PCERT_PRIVATE_KEY_VALIDITY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
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
tech.root: 
req.typenames: CERT_PRIVATE_KEY_VALIDITY, *PCERT_PRIVATE_KEY_VALIDITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CERT_PRIVATE_KEY_VALIDITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_PRIVATE_KEY_VALIDITY structure


## -description


The <b>CERT_PRIVATE_KEY_VALIDITY</b> structure indicates a valid time span for the private key corresponding to a certificate's public key. If the <b>NotBefore</b> component is zero or not present, no statement is made as to when the validity period of the private key begins. If the <b>NotAfter</b> component is zero or not present, no end date is set on the validity of the private key.

A <b>CERT_PRIVATE_KEY_VALIDITY</b> structure is a member of the 
<a href="https://msdn.microsoft.com/cedf0321-4f5a-48a9-abfd-d8642bb89576">CERT_KEY_ATTRIBUTES_INFO</a> structure.


## -struct-fields




### -field NotBefore

Date and time before which the certificate is not valid. For dates between 1950 and 2049 inclusive, the date and time is encoded UTC-time in the form YYMMDDHHMMSS. This member uses a two-digit year and is precise to seconds. For dates before 1950 or after 2049, encoded generalized-time is used. Encoded generalized time is in the form YYYYMMDDHHMMSSMMM, using a four-digit year, and is precise to milliseconds. Even though generalized time supports millisecond resolution, the <b>NotBefore</b> time is only precise to seconds.


### -field NotAfter

Date and time after which the certificate is not valid. For dates between 1950 and 2049 inclusive, the date and time is encoded UTC-time in the form YYMMDDHHMMSS. This member uses a two-digit year and is precise to seconds. For dates before 1950 or after 2049, encoded generalized time is used. Encoded generalized time is in the form YYYYMMDDHHMMSSMMM, using a four digit year, and is precise to milliseconds. Even though generalized time supports millisecond resolution, the <b>NotAfter</b> time is only precise to seconds.


## -see-also




<a href="https://msdn.microsoft.com/cedf0321-4f5a-48a9-abfd-d8642bb89576">CERT_KEY_ATTRIBUTES_INFO</a>
 

 

