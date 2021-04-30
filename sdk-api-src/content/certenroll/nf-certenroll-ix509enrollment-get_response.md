---
UID: NF:certenroll.IX509Enrollment.get_Response
title: IX509Enrollment::get_Response (certenroll.h)
description: Retrieves the certificate response returned from a certification authority.
helpviewer_keywords: ["IX509Enrollment interface [Security]","Response property","IX509Enrollment.Response","IX509Enrollment.get_Response","IX509Enrollment::Response","IX509Enrollment::get_Response","Response property [Security]","Response property [Security]","IX509Enrollment interface","certenroll/IX509Enrollment::Response","certenroll/IX509Enrollment::get_Response","get_Response","security.ix509enrollment_response_property"]
old-location: security\ix509enrollment_response_property.htm
tech.root: security
ms.assetid: 4580d376-0dbb-4418-a542-b0a9710862c4
ms.date: 12/05/2018
ms.keywords: IX509Enrollment interface [Security],Response property, IX509Enrollment.Response, IX509Enrollment.get_Response, IX509Enrollment::Response, IX509Enrollment::get_Response, Response property [Security], Response property [Security],IX509Enrollment interface, certenroll/IX509Enrollment::Response, certenroll/IX509Enrollment::get_Response, get_Response, security.ix509enrollment_response_property
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
 - IX509Enrollment::get_Response
 - certenroll/IX509Enrollment::get_Response
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
 - IX509Enrollment.Response
 - IX509Enrollment.get_Response
---

# IX509Enrollment::get_Response


## -description

The <b>Response</b> property retrieves the certificate response returned from a certification authority. The response is contained in a byte array that is encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) as defined by the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) standard.  The DER-encoded byte array is represented by a string that is  either a pure binary sequence or Unicode encoded.

This property is read-only.

## -parameters

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a>