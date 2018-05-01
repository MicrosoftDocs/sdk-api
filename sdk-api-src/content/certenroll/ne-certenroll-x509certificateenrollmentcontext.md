---
UID: NE:certenroll.X509CertificateEnrollmentContext
title: X509CertificateEnrollmentContext
author: windows-driver-content
description: Specifies the nature of the end entity for which the certificate is intended.
old-location: security\x509certificateenrollmentcontext_enum.htm
old-project: SecCertEnroll
ms.assetid: 2db0e129-a566-47ba-ab57-53c7db09e8e3
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, X509CertificateEnrollmentContext, X509CertificateEnrollmentContext enumeration [Security], certenroll/ContextAdministratorForceMachine, certenroll/ContextMachine, certenroll/ContextUser, certenroll/X509CertificateEnrollmentContext, security.x509certificateenrollmentcontext_enum
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: X509CertificateEnrollmentContext
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	CertEnroll.h
api_name:
-	X509CertificateEnrollmentContext
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# X509CertificateEnrollmentContext enumeration


## -description


The <b>X509CertificateEnrollmentContext</b> enumeration  specifies the nature of the end entity for which the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a> is intended. This enumeration is used by the following interfaces:<ul>
<li>
<a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
</li>
<li>
<a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a>
</li>
</ul>



## -enum-fields




### -field ContextNone


### -field ContextUser

The certificate is intended for an end user.


### -field ContextMachine

The certificate is intended for a computer.


### -field ContextAdministratorForceMachine

The certificate is being requested by an administrator acting on the behalf of a computer.


## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>
 

 

