---
UID: NF:certenroll.IX509CertificateRequest.get_CspInformations
title: IX509CertificateRequest::get_CspInformations
author: windows-sdk-content
description: Specifies and retrieves a collection of cryptographic providers available for use by the request object.
old-location: security\ix509certificaterequest_cspinformations_property.htm
tech.root: SecCertEnroll
ms.assetid: 7be532ab-0ab0-4c22-b274-c925fd5827d5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: CspInformations property [Security], CspInformations property [Security],IX509CertificateRequest interface, IX509CertificateRequest interface [Security],CspInformations property, IX509CertificateRequest.CspInformations, IX509CertificateRequest.get_CspInformations, IX509CertificateRequest::CspInformations, IX509CertificateRequest::get_CspInformations, IX509CertificateRequest::put_CspInformations, certenroll/IX509CertificateRequest::CspInformations, certenroll/IX509CertificateRequest::get_CspInformations, certenroll/IX509CertificateRequest::put_CspInformations, get_CspInformations, security.ix509certificaterequest_cspinformations_property
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
 - IX509CertificateRequest.CspInformations
 - IX509CertificateRequest.get_CspInformations
 - IX509CertificateRequest.put_CspInformations
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequest::get_CspInformations


## -description


The <b>CspInformations</b> property specifies and retrieves a collection of cryptographic providers available for use by the request object.

This property is read/write.


## -parameters


## -remarks



If you want to specify a collection of providers, you must set this property before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa377669(v=VS.85).aspx">Initialize</a> method. The collection that you specify must contain all providers currently installed on the computer. If you specify a subset or a superset, the behavior of this property is undefined.

If you do not specify a collection, the <a href="https://msdn.microsoft.com/en-us/library/Aa377669(v=VS.85).aspx">Initialize</a> method sets the property value to a collection of all providers installed on the computer.

The <b>CspInformations</b> property exists so that the caller can avoid forcing the request object to fill the collection. This is useful when the caller is creating multiple requests in one session.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a>
 

 

