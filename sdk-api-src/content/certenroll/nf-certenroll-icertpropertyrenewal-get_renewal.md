---
UID: NF:certenroll.ICertPropertyRenewal.get_Renewal
title: ICertPropertyRenewal::get_Renewal (certenroll.h)
description: Retrieves the SHA-1 hash of the new certificate.
helpviewer_keywords: ["ICertPropertyRenewal interface [Security]","Renewal property","ICertPropertyRenewal.Renewal","ICertPropertyRenewal.get_Renewal","ICertPropertyRenewal::Renewal","ICertPropertyRenewal::get_Renewal","Renewal property [Security]","Renewal property [Security]","ICertPropertyRenewal interface","certenroll/ICertPropertyRenewal::Renewal","certenroll/ICertPropertyRenewal::get_Renewal","get_Renewal","security.icertpropertyrenewal_renewal_property"]
old-location: security\icertpropertyrenewal_renewal_property.htm
tech.root: security
ms.assetid: f2ea8198-01ec-4485-9f7e-9b9fa8ddba6f
ms.date: 12/05/2018
ms.keywords: ICertPropertyRenewal interface [Security],Renewal property, ICertPropertyRenewal.Renewal, ICertPropertyRenewal.get_Renewal, ICertPropertyRenewal::Renewal, ICertPropertyRenewal::get_Renewal, Renewal property [Security], Renewal property [Security],ICertPropertyRenewal interface, certenroll/ICertPropertyRenewal::Renewal, certenroll/ICertPropertyRenewal::get_Renewal, get_Renewal, security.icertpropertyrenewal_renewal_property
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
 - ICertPropertyRenewal::get_Renewal
 - certenroll/ICertPropertyRenewal::get_Renewal
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
 - ICertPropertyRenewal.Renewal
 - ICertPropertyRenewal.get_Renewal
---

# ICertPropertyRenewal::get_Renewal


## -description

The <b>Renewal</b> property retrieves the SHA-1 hash of the new certificate. The hash is returned in a byte array , and the byte array is represented by a Unicode encoded string.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyrenewal-initialize">Initialize</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyrenewal-initializefromcertificatehash">InitializeFromCertificateHash</a> method to specify a value for the <b>Renewal</b> property.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyrenewal">ICertPropertyRenewal</a>