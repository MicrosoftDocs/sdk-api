---
UID: NF:certenroll.IX509CertificateRequest.get_EnrollmentContext
title: IX509CertificateRequest::get_EnrollmentContext
author: windows-sdk-content
description: Retrieves a value that specifies whether the certificate is intended for a computer or a user.
old-location: security\ix509certificaterequest_enrollmentcontext_property.htm
old-project: SecCertEnroll
ms.assetid: ea0fa54d-0de6-4578-b93a-1e399101006b
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, EnrollmentContext property [Security], EnrollmentContext property [Security],IX509CertificateRequest interface, IX509CertificateRequest interface [Security],EnrollmentContext property, IX509CertificateRequest.EnrollmentContext, IX509CertificateRequest.get_EnrollmentContext, IX509CertificateRequest::EnrollmentContext, IX509CertificateRequest::get_EnrollmentContext, certenroll/IX509CertificateRequest::EnrollmentContext, certenroll/IX509CertificateRequest::get_EnrollmentContext, get_EnrollmentContext, security.ix509certificaterequest_enrollmentcontext_property
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509CertificateRequest.EnrollmentContext
-	IX509CertificateRequest.get_EnrollmentContext
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequest::get_EnrollmentContext


## -description


The <b>EnrollmentContext</b> property retrieves a value that specifies whether the certificate is intended for a computer or a user.

This property is read-only.


## -parameters


## -remarks



For a PKCS #7 or CMC request, the property value is retrieved from the inner request object.




## -see-also




<a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/25774ccb-8e76-443d-89da-177d6e77c019">IX509SignatureInformation</a>
 

 

