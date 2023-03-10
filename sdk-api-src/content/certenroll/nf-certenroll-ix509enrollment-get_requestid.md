---
UID: NF:certenroll.IX509Enrollment.get_RequestId
title: IX509Enrollment::get_RequestId (certenroll.h)
description: Retrieves a unique identifier for the certificate request sent to the certification authority by the Enroll method.
helpviewer_keywords: ["IX509Enrollment interface [Security]","RequestId property","IX509Enrollment.RequestId","IX509Enrollment.get_RequestId","IX509Enrollment::RequestId","IX509Enrollment::get_RequestId","RequestId property [Security]","RequestId property [Security]","IX509Enrollment interface","certenroll/IX509Enrollment::RequestId","certenroll/IX509Enrollment::get_RequestId","get_RequestId","security.ix509enrollment_requestid_property"]
old-location: security\ix509enrollment_requestid_property.htm
tech.root: security
ms.assetid: 64048d5d-36fd-4709-a924-7f84a2b2b97e
ms.date: 12/05/2018
ms.keywords: IX509Enrollment interface [Security],RequestId property, IX509Enrollment.RequestId, IX509Enrollment.get_RequestId, IX509Enrollment::RequestId, IX509Enrollment::get_RequestId, RequestId property [Security], RequestId property [Security],IX509Enrollment interface, certenroll/IX509Enrollment::RequestId, certenroll/IX509Enrollment::get_RequestId, get_RequestId, security.ix509enrollment_requestid_property
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509Enrollment::get_RequestId
 - certenroll/IX509Enrollment::get_RequestId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509Enrollment.RequestId
 - IX509Enrollment.get_RequestId
---

# IX509Enrollment::get_RequestId


## -description

The <b>RequestId</b> property retrieves a unique identifier for the certificate request sent to the certification authority by the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-enroll">Enroll</a> method.

This property is read-only.

## -parameters

## -remarks

The value of the <b>RequestId</b> property is set during the enrollment process. It can be used during subsequent communication between the client and the CA. For example, if a CA marks a request as pending when initially submitted, the client can use the request ID and the configuration string when it again contacts the CA and attempts to retrieve the certificate response. To retrieve the configuration string, call the  <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-get_caconfigstring">CAConfigString</a> property.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a>