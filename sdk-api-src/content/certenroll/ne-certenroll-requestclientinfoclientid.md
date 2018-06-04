---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# RequestClientInfoClientId enumeration


## -description


The <b>RequestClientInfoClientId</b> enumeration  specifies the type of application that created a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate request</a>.  This can be used to initialize a <a href="https://msdn.microsoft.com/82b773e3-7d47-4c85-a6b3-c8ef3e67630a">IX509AttributeClientId</a> object that contains information about the client. It is also used by the <a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a> interface.


## -enum-fields




### -field ClientIdNone

No client identifier is specified.


### -field ClientIdXEnroll2003

Specifies the Certificate Enrollment Control that is available on Windows Server 2003.


### -field ClientIdAutoEnroll2003

Specifies the autoenrollment  that is available on Windows Server 2003.


### -field ClientIdWizard2003

Specifies the Certificate Request Wizard that is available on Windows Server 2003.


### -field ClientIdCertReq2003

Specifies the Certreq.exe command-line tool that is available on Windows Server 2003.


### -field ClientIdDefaultRequest

Specifies the default certificate request object that is available starting with Windows Vista. This is represented by the <a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a> interface and is the default value if the client ID is not set by the caller.


### -field ClientIdAutoEnroll

Specifies the autoenrollment that is available starting with  Windows Vista.


### -field ClientIdRequestWizard

Specifies the Certificate Request Wizard that is available starting with Windows Vista.


### -field ClientIdEOBO

Specifies the Enroll-On-Behalf-Of (EOBO) Wizard that is available starting with Windows Vista.


### -field ClientIdCertReq

Specifies the Certreq.exe command-line tool that is available starting with Windows Vista.


### -field ClientIdTest

This value is not supported.


### -field ClientIdWinRT


### -field ClientIdUserStart

This is the base value for custom applications.


## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/82b773e3-7d47-4c85-a6b3-c8ef3e67630a">IX509AttributeClientId</a>



<a href="https://msdn.microsoft.com/5425c9ab-565d-449d-87e1-e5765868acfb">IX509CertificateRequest</a>
 

 

