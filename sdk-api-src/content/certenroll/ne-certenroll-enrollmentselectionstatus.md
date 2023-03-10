---
UID: NE:certenroll.EnrollmentSelectionStatus
title: EnrollmentSelectionStatus (certenroll.h)
description: Specifies whether the enrollment status of an object will be monitored during the enrollment process.
helpviewer_keywords: ["EnrollmentSelectionStatus","EnrollmentSelectionStatus enumeration [Security]","SelectedNo","SelectedYes","certenroll/EnrollmentSelectionStatus","certenroll/SelectedNo","certenroll/SelectedYes","security.enrollmentselectionstatus_enum"]
old-location: security\enrollmentselectionstatus_enum.htm
tech.root: security
ms.assetid: a762d81b-0426-483c-a9c0-70f531f4b6ac
ms.date: 12/05/2018
ms.keywords: EnrollmentSelectionStatus, EnrollmentSelectionStatus enumeration [Security], SelectedNo, SelectedYes, certenroll/EnrollmentSelectionStatus, certenroll/SelectedNo, certenroll/SelectedYes, security.enrollmentselectionstatus_enum
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: EnrollmentSelectionStatus
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnrollmentSelectionStatus
 - certenroll/EnrollmentSelectionStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - EnrollmentSelectionStatus
---

# EnrollmentSelectionStatus enumeration


## -description

The <b>EnrollmentSelectionStatus</b> enumeration type specifies whether the enrollment status of an object will be monitored during the enrollment process. Cryptographic providers, individual enrollment objects in a collection, and <a href="/windows/desktop/SecGloss/c-gly">certification authorities</a> are often monitored and their status displayed in a user interface. A value of this enumeration can be specified or retrieved by using the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentstatus-get_selected">Selected</a> property on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentstatus">IX509EnrollmentStatus</a> interface. An <b>IX509EnrollmentStatus</b> object can be retrieved from the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> and <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> objects.

## -enum-fields

### -field SelectedNo:0

The enrollment status is not monitored.

### -field SelectedYes:1

The enrollment status is monitored.

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentstatus">IX509EnrollmentStatus</a>
