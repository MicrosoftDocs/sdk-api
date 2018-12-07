---
UID: NF:certenroll.IX509CertificateRequest.get_SuppressDefaults
title: IX509CertificateRequest::get_SuppressDefaults
author: windows-sdk-content
description: Specifies or retrieves a Boolean value that indicates whether the default extensions and attributes are included in the request.
old-location: security\ix509certificaterequest_suppressdefaults_property.htm
tech.root: seccertenroll
ms.assetid: 3a7847b6-52b4-4058-8113-cbc3b9101a5b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509CertificateRequest interface [Security],SuppressDefaults property, IX509CertificateRequest.SuppressDefaults, IX509CertificateRequest.get_SuppressDefaults, IX509CertificateRequest::SuppressDefaults, IX509CertificateRequest::get_SuppressDefaults, IX509CertificateRequest::put_SuppressDefaults, SuppressDefaults property [Security], SuppressDefaults property [Security],IX509CertificateRequest interface, certenroll/IX509CertificateRequest::SuppressDefaults, certenroll/IX509CertificateRequest::get_SuppressDefaults, certenroll/IX509CertificateRequest::put_SuppressDefaults, get_SuppressDefaults, security.ix509certificaterequest_suppressdefaults_property
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
 - IX509CertificateRequest.SuppressDefaults
 - IX509CertificateRequest.get_SuppressDefaults
 - IX509CertificateRequest.put_SuppressDefaults
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequest::get_SuppressDefaults


## -description


The <b>SuppressDefaults</b> property specifies or retrieves a Boolean value that indicates whether the default extensions and attributes are included in the request. The defaults are represented by their <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifiers</a> (OIDs).

This property is read/write.


## -parameters


## -remarks



You must initialize the request object before calling this property. Set this property before calling the <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method to suppress inclusion and encoding of default extensions and attributes in the certificate request.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377123(v=VS.85).aspx">IX509CertificateRequest</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa379050(v=VS.85).aspx">IX509SignatureInformation</a>
 

 

