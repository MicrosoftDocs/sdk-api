---
UID: NF:certenroll.IX509Enrollment.get_NameValuePairs
title: IX509Enrollment::get_NameValuePairs (certenroll.h)
description: Retrieves a collection of name-value pairs associated with the enrollment object.
helpviewer_keywords: ["IX509Enrollment interface [Security]","NameValuePairs property","IX509Enrollment.NameValuePairs","IX509Enrollment.get_NameValuePairs","IX509Enrollment::NameValuePairs","IX509Enrollment::get_NameValuePairs","NameValuePairs property [Security]","NameValuePairs property [Security]","IX509Enrollment interface","certenroll/IX509Enrollment::NameValuePairs","certenroll/IX509Enrollment::get_NameValuePairs","get_NameValuePairs","security.ix509enrollment_namevaluepairs_property"]
old-location: security\ix509enrollment_namevaluepairs_property.htm
tech.root: security
ms.assetid: d682fb7c-de80-4285-baa2-f86c997f0987
ms.date: 12/05/2018
ms.keywords: IX509Enrollment interface [Security],NameValuePairs property, IX509Enrollment.NameValuePairs, IX509Enrollment.get_NameValuePairs, IX509Enrollment::NameValuePairs, IX509Enrollment::get_NameValuePairs, NameValuePairs property [Security], NameValuePairs property [Security],IX509Enrollment interface, certenroll/IX509Enrollment::NameValuePairs, certenroll/IX509Enrollment::get_NameValuePairs, get_NameValuePairs, security.ix509enrollment_namevaluepairs_property
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
 - IX509Enrollment::get_NameValuePairs
 - certenroll/IX509Enrollment::get_NameValuePairs
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
 - IX509Enrollment.NameValuePairs
 - IX509Enrollment.get_NameValuePairs
---

# IX509Enrollment::get_NameValuePairs


## -description

The <b>NameValuePairs</b> property retrieves a collection of name-value pairs associated with the enrollment object.

This property is read-only.

## -parameters

## -remarks

name-value pairs are passed to the certification authority (CA) with the request for the CA to act upon. The <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509namevaluepairs">IX509NameValuePairs</a> object is associated with the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> object when the object is initialized. Therefore, before calling this property, you must initialize the <b>IX509Enrollment</b> object by calling one of the following methods.<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-initialize">Initialize</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-initializefromrequest">InitializeFromRequest</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-initializefromtemplatename">InitializeFromTemplateName</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a>