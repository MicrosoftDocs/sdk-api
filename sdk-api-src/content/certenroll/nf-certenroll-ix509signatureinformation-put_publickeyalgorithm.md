---
UID: NF:certenroll.IX509SignatureInformation.put_PublicKeyAlgorithm
title: IX509SignatureInformation::put_PublicKeyAlgorithm
author: windows-sdk-content
description: Specifies and retrieves an object identifier (OID) for the public key algorithm used in the GetSignatureAlgorithm method.
old-location: security\ix509signatureinformation_publickeyalgorithm_property.htm
tech.root: seccertenroll
ms.assetid: f964328f-15a6-4d8e-a2cf-73c8d74995e8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509SignatureInformation interface [Security],PublicKeyAlgorithm property, IX509SignatureInformation.PublicKeyAlgorithm, IX509SignatureInformation.put_PublicKeyAlgorithm, IX509SignatureInformation::PublicKeyAlgorithm, IX509SignatureInformation::get_PublicKeyAlgorithm, IX509SignatureInformation::put_PublicKeyAlgorithm, PublicKeyAlgorithm property [Security], PublicKeyAlgorithm property [Security],IX509SignatureInformation interface, certenroll/IX509SignatureInformation::PublicKeyAlgorithm, certenroll/IX509SignatureInformation::get_PublicKeyAlgorithm, certenroll/IX509SignatureInformation::put_PublicKeyAlgorithm, put_PublicKeyAlgorithm, security.ix509signatureinformation_publickeyalgorithm_property
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
 - IX509SignatureInformation.PublicKeyAlgorithm
 - IX509SignatureInformation.get_PublicKeyAlgorithm
 - IX509SignatureInformation.put_PublicKeyAlgorithm
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509SignatureInformation::put_PublicKeyAlgorithm


## -description


The <b>PublicKeyAlgorithm</b> property specifies and retrieves an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) for the public key algorithm used in the <a href="https://msdn.microsoft.com/e5b43e74-d802-43ff-bdf2-96ab475c31e7">GetSignatureAlgorithm</a> method.

This property is read/write.


## -parameters


## -remarks



Unless you are retrieving a signature algorithm for a null-signed certificate request, you must set this property before calling the <a href="https://msdn.microsoft.com/e5b43e74-d802-43ff-bdf2-96ab475c31e7">GetSignatureAlgorithm</a> method. You must also set the <a href="https://msdn.microsoft.com/b5242975-50e5-49d6-be1f-3a09ada03593">HashAlgorithm</a> property. You can also set the <a href="https://msdn.microsoft.com/e62ecdf1-56d8-4707-8e5d-deef4d79a34c">AlternateSignatureAlgorithm</a> and <a href="https://msdn.microsoft.com/a693343e-7c9a-4967-b46c-53936497662a">NullSigned</a>   properties.

The <b>PublicKeyAlgorithm</b> property validates whether the OID you specify represents a public key algorithm. If the OID is valid, the property also clears the signature property cache.




## -see-also




<a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>
 

 

