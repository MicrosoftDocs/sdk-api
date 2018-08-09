---
UID: NF:certenroll.ICertPropertyEnrollment.get_RequestId
title: ICertPropertyEnrollment::get_RequestId
author: windows-sdk-content
description: Retrieves a unique certificate request identifier.
old-location: security\icertpropertyenrollment_requestid_property.htm
old-project: seccertenroll
ms.assetid: a9e2000c-7d64-43f1-b891-b5cd6f46201f
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ICertPropertyEnrollment interface [Security],RequestId property, ICertPropertyEnrollment.RequestId, ICertPropertyEnrollment.get_RequestId, ICertPropertyEnrollment::RequestId, ICertPropertyEnrollment::get_RequestId, RequestId property [Security], RequestId property [Security],ICertPropertyEnrollment interface, certenroll/ICertPropertyEnrollment::RequestId, certenroll/ICertPropertyEnrollment::get_RequestId, get_RequestId, security.icertpropertyenrollment_requestid_property
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICertPropertyEnrollment.RequestId
 - ICertPropertyEnrollment.get_RequestId
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertPropertyEnrollment::get_RequestId


## -description


The <b>RequestId</b> property retrieves a unique  certificate request identifier.

This property is read-only.


## -parameters


## -remarks



Set the  <b>RequestId</b> property by calling the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method. The request ID is created during the enrollment process. For more information, see the <a href="https://msdn.microsoft.com/64048d5d-36fd-4709-a924-7f84a2b2b97e">RequestId</a> property on the <a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a> interface.

The ID can be used during subsequent communication between the client and the CA. For example, if a CA marks a request as pending when initially submitted, the client can use the request ID and the configuration string when it again contacts the CA and attempts to retrieve the certificate response.

You can also call the following properties to retrieve the other values specified during initialization:<ul>
<li>
<a href="https://msdn.microsoft.com/5b388cfe-e0b1-4b57-bf6c-81f9ab65ffcf">CADnsName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ea490e37-e1b9-4887-8051-c3447136875c">CAName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a12b7368-cace-47c4-bfd4-08845dc2634c">FriendlyName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>



<a href="https://msdn.microsoft.com/7530998b-b59c-426b-a74a-ead4bca55c3b">ICertPropertyEnrollment</a>
 

 

