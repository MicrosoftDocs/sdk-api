---
UID: NF:certenroll.IX509SignatureInformation.put_HashAlgorithm
title: IX509SignatureInformation::put_HashAlgorithm
author: windows-sdk-content
description: Specifies and retrieves an object identifier (OID) for the hashing algorithm used in the GetSignatureAlgorithm method.
old-location: security\ix509signatureinformation_hashalgorithm_property.htm
old-project: SecCertEnroll
ms.assetid: b5242975-50e5-49d6-be1f-3a09ada03593
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: HashAlgorithm property [Security], HashAlgorithm property [Security],IX509SignatureInformation interface, IX509SignatureInformation interface [Security],HashAlgorithm property, IX509SignatureInformation.HashAlgorithm, IX509SignatureInformation.put_HashAlgorithm, IX509SignatureInformation::HashAlgorithm, IX509SignatureInformation::get_HashAlgorithm, IX509SignatureInformation::put_HashAlgorithm, certenroll/IX509SignatureInformation::HashAlgorithm, certenroll/IX509SignatureInformation::get_HashAlgorithm, certenroll/IX509SignatureInformation::put_HashAlgorithm, put_HashAlgorithm, security.ix509signatureinformation_hashalgorithm_property
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509SignatureInformation.HashAlgorithm
-	IX509SignatureInformation.get_HashAlgorithm
-	IX509SignatureInformation.put_HashAlgorithm
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509SignatureInformation::put_HashAlgorithm


## -description


The <b>HashAlgorithm</b> property specifies and retrieves an <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) for the hashing algorithm used in the <a href="https://msdn.microsoft.com/e5b43e74-d802-43ff-bdf2-96ab475c31e7">GetSignatureAlgorithm</a> method.

This property is read/write.


## -parameters


## -remarks



You must set this property before calling the <a href="https://msdn.microsoft.com/e5b43e74-d802-43ff-bdf2-96ab475c31e7">GetSignatureAlgorithm</a> method. You must also set the <a href="https://msdn.microsoft.com/f964328f-15a6-4d8e-a2cf-73c8d74995e8">PublicKeyAlgorithm</a> property unless you are retrieving a signature algorithm for a null-signed certificate request.  You can also set the <a href="https://msdn.microsoft.com/a693343e-7c9a-4967-b46c-53936497662a">NullSigned</a>, <a href="https://msdn.microsoft.com/e62ecdf1-56d8-4707-8e5d-deef4d79a34c">AlternateSignatureAlgorithm</a>,  and <a href="https://msdn.microsoft.com/library/windows/hardware/dn965807">Parameters</a> properties.

The <b>HashAlgorithm</b> property validates whether the OID you specify represents a hashing algorithm. If the OID is valid, the property also clears the signature property cache.




## -see-also




<a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>
 

 

