---
UID: NS:wincrypt._CERT_ECC_SIGNATURE
title: "_CERT_ECC_SIGNATURE"
author: windows-sdk-content
description: Contains the r and s values for an Elliptic Curve Digital Signature Algorithm (ECDSA) signature.
old-location: security\cert_ecc_signature.htm
tech.root: seccrypto
ms.assetid: f341d839-c06d-40e9-a6ed-79a627918110
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "*PCERT_ECC_SIGNATURE, CERT_ECC_SIGNATURE, CERT_ECC_SIGNATURE structure [Security], PCERT_ECC_SIGNATURE, PCERT_ECC_SIGNATURE structure pointer [Security], _CERT_ECC_SIGNATURE, security.cert_ecc_signature, wincrypt/CERT_ECC_SIGNATURE, wincrypt/PCERT_ECC_SIGNATURE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - Wincrypt.h
api_name:
 - CERT_ECC_SIGNATURE
product: Windows
targetos: Windows
req.typenames: CERT_ECC_SIGNATURE, *PCERT_ECC_SIGNATURE
req.redist: 
---

# _CERT_ECC_SIGNATURE structure


## -description


The <b>CERT_ECC_SIGNATURE</b> structure contains the r and s values for an Elliptic Curve Digital Signature Algorithm (ECDSA) signature.


## -struct-fields




### -field r

The r value of the ECDSA signature. This value is in <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">little-endian</a> order.


### -field s

The s value of the ECDSA signature. This value is in little-endian order.


## -remarks



Before encoding, a leading zero byte will be inserted for the <b>r</b> and <b>s</b> members. After decoding, a leading zero byte will be removed from the <b>r</b> and <b>s</b> members if the leading zero is present.




