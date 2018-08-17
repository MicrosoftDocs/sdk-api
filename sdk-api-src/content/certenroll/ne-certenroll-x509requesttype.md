---
UID: NE:certenroll.X509RequestType
title: X509RequestType
author: windows-sdk-content
description: Specifies the certificate request type.
old-location: security\x509requesttype_enum.htm
old-project: seccertenroll
ms.assetid: e7941e88-b825-409a-87b9-a560aa6d5868
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: TypeAny, TypeCertificate, TypeCmc, TypePkcs10, TypePkcs7, X509RequestType, X509RequestType enumeration [Security], certenroll/TypeAny, certenroll/TypeCertificate, certenroll/TypeCmc, certenroll/TypePkcs10, certenroll/TypePkcs7, certenroll/X509RequestType, security.x509requesttype_enum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: certenroll.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - X509RequestType
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# X509RequestType enumeration


## -description


The <b>X509RequestType</b> enumeration specifies the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate request</a> type. This enumeration is returned by the <a href="https://msdn.microsoft.com/en-us/library/Aa377801(v=VS.85).aspx">Type</a> property on the <a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a> interface.


## -enum-fields




### -field TypeAny

The type is not defined.


### -field TypePkcs10

A PKCS #10 request. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a> interface.


### -field TypePkcs7

A PKCS #7 request represented by an <a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a> interface.


### -field TypeCmc

A <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">Certificate Management over CMS</a> (CMC) request. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a> interface.


### -field TypeCertificate

A self-signed <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate</a>. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a> interface.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374846(v=VS.85).aspx">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>
 

 

