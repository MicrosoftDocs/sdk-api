---
UID: NF:certenroll.IX509PublicKey.get_Algorithm
title: IX509PublicKey::get_Algorithm
author: windows-sdk-content
description: Retrieves an object identifier (OID) for the public key algorithm.
old-location: security\ix509publickey_algorithm_property.htm
tech.root: SecCertEnroll
ms.assetid: 6c34323e-669e-434c-946f-65fe53456a11
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Algorithm property [Security], Algorithm property [Security],IX509PublicKey interface, IX509PublicKey interface [Security],Algorithm property, IX509PublicKey.Algorithm, IX509PublicKey.get_Algorithm, IX509PublicKey::Algorithm, IX509PublicKey::get_Algorithm, certenroll/IX509PublicKey::Algorithm, certenroll/IX509PublicKey::get_Algorithm, get_Algorithm, security.ix509publickey_algorithm_property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
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
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509PublicKey.Algorithm
 - IX509PublicKey.get_Algorithm
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509PublicKey.get_Algorithm
: 
---

# IX509PublicKey::get_Algorithm


## -description


The <b>Algorithm</b> property retrieves an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) for the public key algorithm.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/3e92d934-1ab7-4f09-a579-0dde4ef44c7f">InitializeFromEncodedPublicKeyInfo</a> method or the <a href="https://msdn.microsoft.com/b6db46b2-95f5-4ba9-829d-97bf83fd9806">Initialize</a> method to initialize the public key object before calling this property.




## -see-also




<a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a>
 

 

