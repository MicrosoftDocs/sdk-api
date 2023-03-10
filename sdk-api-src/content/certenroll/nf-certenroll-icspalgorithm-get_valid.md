---
UID: NF:certenroll.ICspAlgorithm.get_Valid
title: ICspAlgorithm::get_Valid (certenroll.h)
description: Retrieves a Boolean value that specifies whether the algorithm object is valid.
helpviewer_keywords: ["ICspAlgorithm interface [Security]","Valid property","ICspAlgorithm.Valid","ICspAlgorithm.get_Valid","ICspAlgorithm::Valid","ICspAlgorithm::get_Valid","Valid property [Security]","Valid property [Security]","ICspAlgorithm interface","certenroll/ICspAlgorithm::Valid","certenroll/ICspAlgorithm::get_Valid","get_Valid","security.icspalgorithm_valid_property"]
old-location: security\icspalgorithm_valid_property.htm
tech.root: security
ms.assetid: 8f8e9f23-f857-49d3-9519-061ccce27514
ms.date: 12/05/2018
ms.keywords: ICspAlgorithm interface [Security],Valid property, ICspAlgorithm.Valid, ICspAlgorithm.get_Valid, ICspAlgorithm::Valid, ICspAlgorithm::get_Valid, Valid property [Security], Valid property [Security],ICspAlgorithm interface, certenroll/ICspAlgorithm::Valid, certenroll/ICspAlgorithm::get_Valid, get_Valid, security.icspalgorithm_valid_property
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
 - ICspAlgorithm::get_Valid
 - certenroll/ICspAlgorithm::get_Valid
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
 - ICspAlgorithm.Valid
 - ICspAlgorithm.get_Valid
---

# ICspAlgorithm::get_Valid


## -description

The <b>Valid</b> property retrieves a Boolean value that specifies whether the algorithm object is valid.

This property is read-only.

## -parameters

## -remarks

If a template refers to an algorithm that is not supported by the specified cryptographic provider, the enrollment process creates a placeholder <a href="/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a> object, sets the <b>Valid</b> property to false, and sets the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspalgorithm-get_name">Name</a> property. No other property values are defined.

You must call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-initializefromname">InitializeFromName</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-initializefromtype">InitializeFromType</a> method on the <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> interface before calling this property.

<a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) is defined by the X.680 through X.683 standards. The Certificate Enrollment API verifies an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) by <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) encoding it and then decoding the result to make certain that the OID remains unchanged and by checking that the following are true:<ul>
<li>The first number in the OID is either 0, 1, or 2.</li>
<li>All other characters are either digits (0 to 9) or periods (.).</li>
<li>No periods start or end the OID.</li>
<li>No consecutive characters are both periods.</li>
<li>The OID must contain at least one period.</li>
<li>If the first number is 0 or 1, the second number must be between 0 and 39 inclusive.</li>
<li>If the first number is 2, the second number can be any value.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspalgorithm">ICspAlgorithm</a>