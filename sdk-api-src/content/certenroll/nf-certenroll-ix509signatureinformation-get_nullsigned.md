---
UID: NF:certenroll.IX509SignatureInformation.get_NullSigned
title: IX509SignatureInformation::get_NullSigned
author: windows-sdk-content
description: Specifies and retrieves a Boolean value that indicates whether the certificate request is null-signed.
old-location: security\ix509signatureinformation_nullsigned_property.htm
tech.root: SecCertEnroll
ms.assetid: a693343e-7c9a-4967-b46c-53936497662a
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509SignatureInformation interface [Security],NullSigned property, IX509SignatureInformation.NullSigned, IX509SignatureInformation.get_NullSigned, IX509SignatureInformation::NullSigned, IX509SignatureInformation::get_NullSigned, IX509SignatureInformation::put_NullSigned, NullSigned property [Security], NullSigned property [Security],IX509SignatureInformation interface, certenroll/IX509SignatureInformation::NullSigned, certenroll/IX509SignatureInformation::get_NullSigned, certenroll/IX509SignatureInformation::put_NullSigned, get_NullSigned, security.ix509signatureinformation_nullsigned_property
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
 - IX509SignatureInformation.NullSigned
 - IX509SignatureInformation.get_NullSigned
 - IX509SignatureInformation.put_NullSigned
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
- IX509SignatureInformation.get_NullSigned
: 
---

# IX509SignatureInformation::get_NullSigned


## -description


The <b>NullSigned</b> property specifies and retrieves a Boolean value that indicates whether the certificate request is null-signed.

This property is read/write.


## -parameters


## -remarks



A null-signed certificate request is not really signed. That is, the request can be digested by using a digest algorithm such as SHA-1, but it is not encrypted with a public key algorithm such as RSA. You must set this property before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa379053(v=VS.85).aspx">GetSignatureAlgorithm</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a>
 

 

