---
UID: NF:certenroll.IX509CertificateRequest.get_EnrollmentContext
title: IX509CertificateRequest::get_EnrollmentContext
author: windows-sdk-content
description: Retrieves a value that specifies whether the certificate is intended for a computer or a user.
old-location: security\ix509certificaterequest_enrollmentcontext_property.htm
tech.root: seccertenroll
ms.assetid: ea0fa54d-0de6-4578-b93a-1e399101006b
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ContextAdministratorForceMachine, ContextMachine, ContextUser, EnrollmentContext property [Security], EnrollmentContext property [Security],IX509CertificateRequest interface, IX509CertificateRequest interface [Security],EnrollmentContext property, IX509CertificateRequest.EnrollmentContext, IX509CertificateRequest.get_EnrollmentContext, IX509CertificateRequest::EnrollmentContext, IX509CertificateRequest::get_EnrollmentContext, certenroll/IX509CertificateRequest::EnrollmentContext, certenroll/IX509CertificateRequest::get_EnrollmentContext, get_EnrollmentContext, security.ix509certificaterequest_enrollmentcontext_property
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
 - IX509CertificateRequest.EnrollmentContext
 - IX509CertificateRequest.get_EnrollmentContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequest::get_EnrollmentContext


## -description


The <b>EnrollmentContext</b> property retrieves a value that specifies whether the certificate is intended for a computer or a user.

This property is read-only.


## -parameters


## -remarks



For a PKCS #7 or CMC request, the property value is retrieved from the inner request object.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a>
 

 

