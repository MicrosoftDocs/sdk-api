---
UID: NF:certenroll.IX509Enrollment.get_RequestId
title: IX509Enrollment::get_RequestId method
author: windows-driver-content
description: Retrieves a unique identifier for the certificate request sent to the certification authority by the Enroll method.
old-location: security\ix509enrollment_requestid_property.htm
old-project: SecCertEnroll
ms.assetid: 64048d5d-36fd-4709-a924-7f84a2b2b97e
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: IX509Enrollment, IX509Enrollment interface [Security], RequestId property, IX509Enrollment.RequestId, IX509Enrollment::get_RequestId, RequestId property [Security], RequestId property [Security], IX509Enrollment interface, certenroll/IX509Enrollment::RequestId, certenroll/IX509Enrollment::get_RequestId, get_RequestId,IX509Enrollment.get_RequestId, security.ix509enrollment_requestid_property
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509Enrollment.RequestId
-	IX509Enrollment.get_RequestId
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509Enrollment::get_RequestId method


## -description


The <b>RequestId</b> property retrieves a unique identifier for the certificate request sent to the certification authority by the <a href="https://msdn.microsoft.com/63abecac-39f4-497a-8851-7a2260abc3dd">Enroll</a> method.

This property is read-only.


## -parameters


## -remarks



The value of the <b>RequestId</b> property is set during the enrollment process. It can be used during subsequent communication between the client and the CA. For example, if a CA marks a request as pending when initially submitted, the client can use the request ID and the configuration string when it again contacts the CA and attempts to retrieve the certificate response. To retrieve the configuration string, call the  <a href="https://msdn.microsoft.com/4a4478c8-a665-4ee1-9f3a-cad259e1c9ce">CAConfigString</a> property.




## -see-also




<a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a>
 

 

