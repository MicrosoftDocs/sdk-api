---
UID: NS:wincrypt._CERT_ISSUER_SERIAL_NUMBER
title: "_CERT_ISSUER_SERIAL_NUMBER"
author: windows-driver-content
description: Acts as a unique identifier of a certificate containing the issuer and issuer's serial number for a certificate.
old-location: security\cert_issuer_serial_number.htm
old-project: SecCrypto
ms.assetid: 4e44113f-81e7-4551-bf4d-50986d6d57bb
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: "*PCERT_ISSUER_SERIAL_NUMBER, CERT_ISSUER_SERIAL_NUMBER, CERT_ISSUER_SERIAL_NUMBER structure [Security], PCERT_ISSUER_SERIAL_NUMBER, PCERT_ISSUER_SERIAL_NUMBER structure pointer [Security], _CERT_ISSUER_SERIAL_NUMBER, _crypto2_cert_issuer_serial_number, security.cert_issuer_serial_number, wincrypt/CERT_ISSUER_SERIAL_NUMBER, wincrypt/PCERT_ISSUER_SERIAL_NUMBER"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CERT_ISSUER_SERIAL_NUMBER, *PCERT_ISSUER_SERIAL_NUMBER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CERT_ISSUER_SERIAL_NUMBER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_ISSUER_SERIAL_NUMBER structure


## -description


The <b>CERT_ISSUER_SERIAL_NUMBER</b> structure acts as a unique identifier of a certificate containing the issuer and issuer's serial number for a certificate.


## -struct-fields




### -field Issuer

A <a href="https://msdn.microsoft.com/2e570727-7da0-4e17-bf5d-6fe0e6aef65b">BLOB</a> structure that contains the name of the issuer.


### -field SerialNumber

A <a href="https://msdn.microsoft.com/7a06eae5-96d8-4ece-98cb-cf0710d2ddbd">CRYPT_INTEGER_BLOB</a> structure that contains the serial number of the certificate. The combination of the issuer name and the serial number is a unique identifier of a certificate.

