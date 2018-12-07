---
UID: NF:certenroll.IX509SignatureInformation.get_HashAlgorithm
title: IX509SignatureInformation::get_HashAlgorithm
author: windows-sdk-content
description: Specifies and retrieves an object identifier (OID) for the hashing algorithm used in the GetSignatureAlgorithm method.
old-location: security\ix509signatureinformation_hashalgorithm_property.htm
tech.root: seccertenroll
ms.assetid: b5242975-50e5-49d6-be1f-3a09ada03593
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: HashAlgorithm property [Security], HashAlgorithm property [Security],IX509SignatureInformation interface, IX509SignatureInformation interface [Security],HashAlgorithm property, IX509SignatureInformation.HashAlgorithm, IX509SignatureInformation.get_HashAlgorithm, IX509SignatureInformation::HashAlgorithm, IX509SignatureInformation::get_HashAlgorithm, IX509SignatureInformation::put_HashAlgorithm, certenroll/IX509SignatureInformation::HashAlgorithm, certenroll/IX509SignatureInformation::get_HashAlgorithm, certenroll/IX509SignatureInformation::put_HashAlgorithm, get_HashAlgorithm, security.ix509signatureinformation_hashalgorithm_property
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
 - IX509SignatureInformation.HashAlgorithm
 - IX509SignatureInformation.get_HashAlgorithm
 - IX509SignatureInformation.put_HashAlgorithm
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509SignatureInformation::get_HashAlgorithm


## -description


The <b>HashAlgorithm</b> property specifies and retrieves an <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) for the hashing algorithm used in the <a href="https://msdn.microsoft.com/en-us/library/Aa379053(v=VS.85).aspx">GetSignatureAlgorithm</a> method.

This property is read/write.


## -parameters


## -remarks



You must set this property before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa379053(v=VS.85).aspx">GetSignatureAlgorithm</a> method. You must also set the <a href="https://msdn.microsoft.com/en-us/library/Aa379059(v=VS.85).aspx">PublicKeyAlgorithm</a> property unless you are retrieving a signature algorithm for a null-signed certificate request.  You can also set the <a href="https://msdn.microsoft.com/en-us/library/Aa379056(v=VS.85).aspx">NullSigned</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa965846(v=VS.85).aspx">AlternateSignatureAlgorithm</a>,  and <a href="https://msdn.microsoft.com/en-us/library/Aa379057(v=VS.85).aspx">Parameters</a> properties.

The <b>HashAlgorithm</b> property validates whether the OID you specify represents a hashing algorithm. If the OID is valid, the property also clears the signature property cache.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a>
 

 

