---
UID: NE:certenroll.WebEnrollmentFlags
title: WebEnrollmentFlags (certenroll.h)
description: Specifies web enrollment behavior.
helpviewer_keywords: ["EnrollPrompt","WebEnrollmentFlags","WebEnrollmentFlags enumeration [Security]","certenroll/EnrollPrompt","certenroll/WebEnrollmentFlags","security.webenrollmentflags"]
old-location: security\webenrollmentflags.htm
tech.root: security
ms.assetid: 3b5940c4-f262-498e-82ab-c56af13afd06
ms.date: 12/05/2018
ms.keywords: EnrollPrompt, WebEnrollmentFlags, WebEnrollmentFlags enumeration [Security], certenroll/EnrollPrompt, certenroll/WebEnrollmentFlags, security.webenrollmentflags
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
req.typenames: WebEnrollmentFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WebEnrollmentFlags
 - certenroll/WebEnrollmentFlags
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
 - WebEnrollmentFlags
---

# WebEnrollmentFlags enumeration


## -description

The <b>WebEnrollmentFlags</b> enumeration specifies web enrollment behavior. It is used by the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmenthelper-enroll">Enroll</a> method on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmenthelper">IX509EnrollmentHelper</a> interface.

## -enum-fields

### -field EnrollPrompt:0x1

If this flag is set and no authentication credential is available for the certificate enrollment server, the certificate service prompts for a credential. If there is no authentication credential and this flag is not set, the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmenthelper-enroll">Enroll</a> method fails.

## -see-also

<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmenthelper-enroll">Enroll</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmenthelper">IX509EnrollmentHelper</a>
