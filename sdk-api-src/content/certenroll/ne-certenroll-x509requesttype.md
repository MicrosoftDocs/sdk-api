---
UID: NE:certenroll.X509RequestType
title: X509RequestType (certenroll.h)
description: Specifies the certificate request type.
old-location: security\x509requesttype_enum.htm
tech.root: seccertenroll
ms.assetid: e7941e88-b825-409a-87b9-a560aa6d5868
ms.date: 12/05/2018
ms.keywords: TypeAny, TypeCertificate, TypeCmc, TypePkcs10, TypePkcs7, X509RequestType, X509RequestType enumeration [Security], certenroll/TypeAny, certenroll/TypeCertificate, certenroll/TypeCmc, certenroll/TypePkcs10, certenroll/TypePkcs7, certenroll/X509RequestType, security.x509requesttype_enum
f1_keywords:
- certenroll/X509RequestType
dev_langs:
- c++
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- CertEnroll.h
api_name:
- X509RequestType
targetos: Windows
req.typenames: X509RequestType
req.redist: 
ms.custom: 19H1
---

# X509RequestType enumeration


## -description


The <b>X509RequestType</b> enumeration specifies the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate request</a> type. This enumeration is returned by the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequest-get_type">Type</a> property on the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequest">IX509CertificateRequest</a> interface.


## -enum-fields




### -field TypeAny

The type is not defined.


### -field TypePkcs10

A PKCS #10 request. For more information, see the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> interface.


### -field TypePkcs7

A PKCS #7 request represented by an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs7">IX509CertificateRequestPkcs7</a> interface.


### -field TypeCmc

A <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">Certificate Management over CMS</a> (CMC) request. For more information, see the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcmc">IX509CertificateRequestCmc</a> interface.


### -field TypeCertificate

A self-signed <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate</a>. For more information, see the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestcertificate">IX509CertificateRequestCertificate</a> interface.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>
 

 

