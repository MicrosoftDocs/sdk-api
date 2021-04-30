---
UID: NF:certenroll.IX509Enrollment2.get_RequestIdString
title: IX509Enrollment2::get_RequestIdString (certenroll.h)
description: Retrieves a string that contains a unique identifier for the certificate request sent to the certification enrollment server (CES).
helpviewer_keywords: ["IX509Enrollment2 interface [Security]","RequestIdString property","IX509Enrollment2.RequestIdString","IX509Enrollment2.get_RequestIdString","IX509Enrollment2::RequestIdString","IX509Enrollment2::get_RequestIdString","RequestIdString property [Security]","RequestIdString property [Security]","IX509Enrollment2 interface","certenroll/IX509Enrollment2::RequestIdString","certenroll/IX509Enrollment2::get_RequestIdString","get_RequestIdString","security.ix509enrollment2_requestidstring"]
old-location: security\ix509enrollment2_requestidstring.htm
tech.root: security
ms.assetid: a1269b0d-6b55-47ba-bca8-610c1032ecc4
ms.date: 12/05/2018
ms.keywords: IX509Enrollment2 interface [Security],RequestIdString property, IX509Enrollment2.RequestIdString, IX509Enrollment2.get_RequestIdString, IX509Enrollment2::RequestIdString, IX509Enrollment2::get_RequestIdString, RequestIdString property [Security], RequestIdString property [Security],IX509Enrollment2 interface, certenroll/IX509Enrollment2::RequestIdString, certenroll/IX509Enrollment2::get_RequestIdString, get_RequestIdString, security.ix509enrollment2_requestidstring
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509Enrollment2::get_RequestIdString
 - certenroll/IX509Enrollment2::get_RequestIdString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - IX509Enrollment2.RequestIdString
 - IX509Enrollment2.get_RequestIdString
---

# IX509Enrollment2::get_RequestIdString


## -description

The <b>RequestIdString</b> property retrieves a string that contains a unique identifier for the certificate request sent to the certification enrollment server (CES).

This property is read-only.

## -parameters

## -remarks

The value of the <b>RequestIdString</b> property is set during the enrollment process. It can be used during subsequent communication between the client and the CES. For example, if a CES marks a request as pending when initially submitted, the client can use the request ID string when it again contacts the CES and attempts to retrieve the certificate response.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment2">IX509Enrollment2</a>