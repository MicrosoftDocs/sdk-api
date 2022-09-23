---
UID: NF:certenroll.ICertPropertyEnrollment.get_FriendlyName
title: ICertPropertyEnrollment::get_FriendlyName (certenroll.h)
description: Retrieves the display name of the certificate. (ICertPropertyEnrollment.get_FriendlyName)
helpviewer_keywords: ["FriendlyName property [Security]","FriendlyName property [Security]","ICertPropertyEnrollment interface","ICertPropertyEnrollment interface [Security]","FriendlyName property","ICertPropertyEnrollment.FriendlyName","ICertPropertyEnrollment.get_FriendlyName","ICertPropertyEnrollment::FriendlyName","ICertPropertyEnrollment::get_FriendlyName","certenroll/ICertPropertyEnrollment::FriendlyName","certenroll/ICertPropertyEnrollment::get_FriendlyName","get_FriendlyName","security.icertpropertyenrollment_friendlyname_property"]
old-location: security\icertpropertyenrollment_friendlyname_property.htm
tech.root: security
ms.assetid: a12b7368-cace-47c4-bfd4-08845dc2634c
ms.date: 12/05/2018
ms.keywords: FriendlyName property [Security], FriendlyName property [Security],ICertPropertyEnrollment interface, ICertPropertyEnrollment interface [Security],FriendlyName property, ICertPropertyEnrollment.FriendlyName, ICertPropertyEnrollment.get_FriendlyName, ICertPropertyEnrollment::FriendlyName, ICertPropertyEnrollment::get_FriendlyName, certenroll/ICertPropertyEnrollment::FriendlyName, certenroll/ICertPropertyEnrollment::get_FriendlyName, get_FriendlyName, security.icertpropertyenrollment_friendlyname_property
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
 - ICertPropertyEnrollment::get_FriendlyName
 - certenroll/ICertPropertyEnrollment::get_FriendlyName
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
 - ICertPropertyEnrollment.FriendlyName
 - ICertPropertyEnrollment.get_FriendlyName
---

# ICertPropertyEnrollment::get_FriendlyName


## -description

The <b>FriendlyName</b> property retrieves the display name of the certificate.

This property is read-only.

## -parameters

## -remarks

Set the  <b>FriendlyName</b> property by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-initialize">Initialize</a> method. The display name is specified during the enrollment process. For more information, see the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-get_certificatefriendlyname">CertificateFriendlyName</a> property on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> interface.

You can also call the following properties to retrieve the other values specified during initialization:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-get_cadnsname">CADnsName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-get_caname">CAName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollment-get_requestid">RequestId</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollment">ICertPropertyEnrollment</a>
