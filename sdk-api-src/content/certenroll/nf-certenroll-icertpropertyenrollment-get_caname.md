---
UID: NF:certenroll.ICertPropertyEnrollment.get_CAName
title: ICertPropertyEnrollment::get_CAName (certenroll.h)
description: Retrieves the common name (CN) of the certification authority (CA).
helpviewer_keywords: ["CAName property [Security]","CAName property [Security]","ICertPropertyEnrollment interface","ICertPropertyEnrollment interface [Security]","CAName property","ICertPropertyEnrollment.CAName","ICertPropertyEnrollment.get_CAName","ICertPropertyEnrollment::CAName","ICertPropertyEnrollment::get_CAName","certenroll/ICertPropertyEnrollment::CAName","certenroll/ICertPropertyEnrollment::get_CAName","get_CAName","security.icertpropertyenrollment_caname_property"]
old-location: security\icertpropertyenrollment_caname_property.htm
tech.root: security
ms.assetid: ea490e37-e1b9-4887-8051-c3447136875c
ms.date: 12/05/2018
ms.keywords: CAName property [Security], CAName property [Security],ICertPropertyEnrollment interface, ICertPropertyEnrollment interface [Security],CAName property, ICertPropertyEnrollment.CAName, ICertPropertyEnrollment.get_CAName, ICertPropertyEnrollment::CAName, ICertPropertyEnrollment::get_CAName, certenroll/ICertPropertyEnrollment::CAName, certenroll/ICertPropertyEnrollment::get_CAName, get_CAName, security.icertpropertyenrollment_caname_property
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
 - ICertPropertyEnrollment::get_CAName
 - certenroll/ICertPropertyEnrollment::get_CAName
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
 - ICertPropertyEnrollment.CAName
 - ICertPropertyEnrollment.get_CAName
---

# ICertPropertyEnrollment::get_CAName


## -description

The <b>CAName</b> property retrieves the common name (CN) of the certification authority (CA).

This property is read-only.

## -parameters

## -remarks

Set the  <b>CAName</b> property by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-initialize">Initialize</a> method. The common name is returned to the client during the enrollment process and is part of the certification authority  configuration string. For more information, see the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-get_caconfigstring">CAConfigString</a> property on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> interface.

You can also call the following properties to retrieve the other values specified during initialization:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-get_cadnsname">CADnsName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-get_friendlyname">FriendlyName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-get_requestid">RequestId</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollment">ICertPropertyEnrollment</a>