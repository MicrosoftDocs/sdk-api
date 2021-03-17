---
UID: NF:certenroll.ICertPropertyEnrollment.get_CADnsName
title: ICertPropertyEnrollment::get_CADnsName (certenroll.h)
description: Retrieves the Domain Naming System (DNS) name of the certification authority (CA).
helpviewer_keywords: ["CADnsName property [Security]","CADnsName property [Security]","ICertPropertyEnrollment interface","ICertPropertyEnrollment interface [Security]","CADnsName property","ICertPropertyEnrollment.CADnsName","ICertPropertyEnrollment.get_CADnsName","ICertPropertyEnrollment::CADnsName","ICertPropertyEnrollment::get_CADnsName","certenroll/ICertPropertyEnrollment::CADnsName","certenroll/ICertPropertyEnrollment::get_CADnsName","get_CADnsName","security.icertpropertyenrollment_cadnsname_property"]
old-location: security\icertpropertyenrollment_cadnsname_property.htm
tech.root: security
ms.assetid: 5b388cfe-e0b1-4b57-bf6c-81f9ab65ffcf
ms.date: 12/05/2018
ms.keywords: CADnsName property [Security], CADnsName property [Security],ICertPropertyEnrollment interface, ICertPropertyEnrollment interface [Security],CADnsName property, ICertPropertyEnrollment.CADnsName, ICertPropertyEnrollment.get_CADnsName, ICertPropertyEnrollment::CADnsName, ICertPropertyEnrollment::get_CADnsName, certenroll/ICertPropertyEnrollment::CADnsName, certenroll/ICertPropertyEnrollment::get_CADnsName, get_CADnsName, security.icertpropertyenrollment_cadnsname_property
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
 - ICertPropertyEnrollment::get_CADnsName
 - certenroll/ICertPropertyEnrollment::get_CADnsName
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
 - ICertPropertyEnrollment.CADnsName
 - ICertPropertyEnrollment.get_CADnsName
---

# ICertPropertyEnrollment::get_CADnsName


## -description

The <b>CADnsName</b> property retrieves the Domain Naming System (DNS) name of the certification authority (CA).

This property is read-only.

## -parameters

## -remarks

Set the  <b>CADnsName</b> property by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-initialize">Initialize</a> method. The DNS name is returned to the client during the enrollment process and is part of the CA  configuration string. For more information, see the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-get_caconfigstring">CAConfigString</a> property on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> interface.

You can also call the following properties to retrieve the other values specified during initialization:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-get_caname">CAName</a>
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