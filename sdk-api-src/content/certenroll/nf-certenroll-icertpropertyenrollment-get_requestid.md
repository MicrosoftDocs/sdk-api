---
UID: NF:certenroll.ICertPropertyEnrollment.get_RequestId
title: ICertPropertyEnrollment::get_RequestId (certenroll.h)
description: Retrieves a unique certificate request identifier.
helpviewer_keywords: ["ICertPropertyEnrollment interface [Security]","RequestId property","ICertPropertyEnrollment.RequestId","ICertPropertyEnrollment.get_RequestId","ICertPropertyEnrollment::RequestId","ICertPropertyEnrollment::get_RequestId","RequestId property [Security]","RequestId property [Security]","ICertPropertyEnrollment interface","certenroll/ICertPropertyEnrollment::RequestId","certenroll/ICertPropertyEnrollment::get_RequestId","get_RequestId","security.icertpropertyenrollment_requestid_property"]
old-location: security\icertpropertyenrollment_requestid_property.htm
tech.root: security
ms.assetid: a9e2000c-7d64-43f1-b891-b5cd6f46201f
ms.date: 12/05/2018
ms.keywords: ICertPropertyEnrollment interface [Security],RequestId property, ICertPropertyEnrollment.RequestId, ICertPropertyEnrollment.get_RequestId, ICertPropertyEnrollment::RequestId, ICertPropertyEnrollment::get_RequestId, RequestId property [Security], RequestId property [Security],ICertPropertyEnrollment interface, certenroll/ICertPropertyEnrollment::RequestId, certenroll/ICertPropertyEnrollment::get_RequestId, get_RequestId, security.icertpropertyenrollment_requestid_property
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
 - ICertPropertyEnrollment::get_RequestId
 - certenroll/ICertPropertyEnrollment::get_RequestId
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
 - ICertPropertyEnrollment.RequestId
 - ICertPropertyEnrollment.get_RequestId
---

# ICertPropertyEnrollment::get_RequestId


## -description

The <b>RequestId</b> property retrieves a unique  certificate request identifier.

This property is read-only.

## -parameters

## -remarks

Set the  <b>RequestId</b> property by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-initialize">Initialize</a> method. The request ID is created during the enrollment process. For more information, see the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-get_requestid">RequestId</a> property on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> interface.

The ID can be used during subsequent communication between the client and the CA. For example, if a CA marks a request as pending when initially submitted, the client can use the request ID and the configuration string when it again contacts the CA and attempts to retrieve the certificate response.

You can also call the following properties to retrieve the other values specified during initialization:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-get_cadnsname">CADnsName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-get_caname">CAName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-get_friendlyname">FriendlyName</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollment">ICertPropertyEnrollment</a>