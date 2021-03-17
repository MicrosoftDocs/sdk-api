---
UID: NF:certenroll.IX509Enrollment.get_Request
title: IX509Enrollment::get_Request (certenroll.h)
description: Retrieves the certificate request associated with the enrollment object.
helpviewer_keywords: ["IX509Enrollment interface [Security]","Request property","IX509Enrollment.Request","IX509Enrollment.get_Request","IX509Enrollment::Request","IX509Enrollment::get_Request","Request property [Security]","Request property [Security]","IX509Enrollment interface","certenroll/IX509Enrollment::Request","certenroll/IX509Enrollment::get_Request","get_Request","security.ix509enrollment_request_property"]
old-location: security\ix509enrollment_request_property.htm
tech.root: security
ms.assetid: dc754240-9c52-459e-9612-caf19eeb351c
ms.date: 12/05/2018
ms.keywords: IX509Enrollment interface [Security],Request property, IX509Enrollment.Request, IX509Enrollment.get_Request, IX509Enrollment::Request, IX509Enrollment::get_Request, Request property [Security], Request property [Security],IX509Enrollment interface, certenroll/IX509Enrollment::Request, certenroll/IX509Enrollment::get_Request, get_Request, security.ix509enrollment_request_property
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
 - IX509Enrollment::get_Request
 - certenroll/IX509Enrollment::get_Request
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
 - IX509Enrollment.Request
 - IX509Enrollment.get_Request
---

# IX509Enrollment::get_Request


## -description

The <b>Request</b> property retrieves the certificate request associated with the enrollment object.

This property is read-only.

## -parameters

## -remarks

This property can be set when the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-initializefromrequest">InitializeFromRequest</a> method is called.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a>