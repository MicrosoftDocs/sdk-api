---
UID: NE:certenroll.PolicyServerUrlFlags
title: PolicyServerUrlFlags (certenroll.h)
description: Contains certificate enrollment policy (CEP) server flags.
helpviewer_keywords: ["PolicyServerUrlFlags","PolicyServerUrlFlags enumeration [Security]","PsfAllowUnTrustedCA","PsfAutoEnrollmentEnabled","PsfLocationGroupPolicy","PsfLocationRegistry","PsfNone","PsfUseClientId","certenroll/PolicyServerUrlFlags","certenroll/PsfAllowUnTrustedCA","certenroll/PsfAutoEnrollmentEnabled","certenroll/PsfLocationGroupPolicy","certenroll/PsfLocationRegistry","certenroll/PsfNone","certenroll/PsfUseClientId","security.policyserverurlflags"]
old-location: security\policyserverurlflags.htm
tech.root: security
ms.assetid: e73bccb8-ca4d-4007-bdf3-1194ede5fdd1
ms.date: 12/05/2018
ms.keywords: PolicyServerUrlFlags, PolicyServerUrlFlags enumeration [Security], PsfAllowUnTrustedCA, PsfAutoEnrollmentEnabled, PsfLocationGroupPolicy, PsfLocationRegistry, PsfNone, PsfUseClientId, certenroll/PolicyServerUrlFlags, certenroll/PsfAllowUnTrustedCA, certenroll/PsfAutoEnrollmentEnabled, certenroll/PsfLocationGroupPolicy, certenroll/PsfLocationRegistry, certenroll/PsfNone, certenroll/PsfUseClientId, security.policyserverurlflags
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: PolicyServerUrlFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PolicyServerUrlFlags
 - certenroll/PolicyServerUrlFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Certenroll.h
api_name:
 - PolicyServerUrlFlags
---

# PolicyServerUrlFlags enumeration


## -description

The <b>PolicyServerUrlFlags</b> enumeration contains certificate enrollment policy (CEP) server flags. It is used by the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollmentpolicyserver-initialize">Initialize</a> method on the <a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver">ICertPropertyEnrollmentPolicyServer</a> interface.

## -enum-fields

### -field PsfNone:0

No flags are specified.

### -field PsfLocationGroupPolicy:1

Policy information is specified in group policy by an administrator.

### -field PsfLocationRegistry:2

Policy information is specified in the registry.

### -field PsfUseClientId:4

Specifies that certificate enrollments and renewals include client specific data in a <b>ClientId</b> attribute. Examples include the name of the cryptographic service provider, the Windows version number, the user name, the computer DNS name, and the domain controller DNS name. This flag can be set by group policy.

This flag has been included to address privacy concerns that can arise during enrollment to servers that are managed by administrators other than those who manage the forest in which the user resides. By not setting this flag, you can prevent sending personal information to non-local administrators.

### -field PsfAutoEnrollmentEnabled:16

Automatic certificate enrollment is enabled.

### -field PsfAllowUnTrustedCA:32

Specifies that the certificate of the issuing CA need not be trusted by the client to install a certificate signed by the CA.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver">ICertPropertyEnrollmentPolicyServer</a>



<a href="/windows/desktop/api/certenroll/nf-certenroll-icertpropertyenrollmentpolicyserver-initialize">Initialize</a>
