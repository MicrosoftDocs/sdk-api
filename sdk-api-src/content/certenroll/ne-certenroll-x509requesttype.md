---
UID: NE:certenroll.X509RequestType
title: X509RequestType
author: windows-sdk-content
description: Specifies the certificate request type.
old-location: security\x509requesttype_enum.htm
old-project: SecCertEnroll
ms.assetid: e7941e88-b825-409a-87b9-a560aa6d5868
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: TypeAny, TypeCertificate, TypeCmc, TypePkcs10, TypePkcs7, X509RequestType, X509RequestType enumeration [Security], certenroll/TypeAny, certenroll/TypeCertificate, certenroll/TypeCmc, certenroll/TypePkcs10, certenroll/TypePkcs7, certenroll/X509RequestType, security.x509requesttype_enum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
-	HeaderDef
api_location:
-	CertEnroll.h
api_name:
-	X509RequestType
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# X509RequestType enumeration


## -description


The <b>X509RequestType</b> enumeration specifies the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a> type. This enumeration is returned by the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a> property on the <a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a> interface.


## -enum-fields




### -field TypeAny

The type is not defined.


### -field TypePkcs10

A PKCS #10 request. For more information, see the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> interface.


### -field TypePkcs7

A PKCS #7 request represented by an <a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a> interface.


### -field TypeCmc

A <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">Certificate Management over CMS</a> (CMC) request. For more information, see the <a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a> interface.


### -field TypeCertificate

A self-signed <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a>. For more information, see the <a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a> interface.


## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>
 

 

