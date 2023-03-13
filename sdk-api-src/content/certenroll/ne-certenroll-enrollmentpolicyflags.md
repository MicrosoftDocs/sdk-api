---
UID: NE:certenroll.EnrollmentPolicyFlags
title: EnrollmentPolicyFlags (certenroll.h)
description: Specifies group policy flags.
helpviewer_keywords: ["DisableGroupPolicyList","DisableUserServerList","EnrollmentPolicyFlags","EnrollmentPolicyFlags enumeration [Security]","certenroll/DisableGroupPolicyList","certenroll/DisableUserServerList","certenroll/EnrollmentPolicyFlags","security.enrollmentpolicyflags"]
old-location: security\enrollmentpolicyflags.htm
tech.root: security
ms.assetid: 07f80422-6856-4371-946f-88efdd9c765a
ms.date: 12/05/2018
ms.keywords: DisableGroupPolicyList, DisableUserServerList, EnrollmentPolicyFlags, EnrollmentPolicyFlags enumeration [Security], certenroll/DisableGroupPolicyList, certenroll/DisableUserServerList, certenroll/EnrollmentPolicyFlags, security.enrollmentpolicyflags
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EnrollmentPolicyFlags
 - certenroll/EnrollmentPolicyFlags
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
 - EnrollmentPolicyFlags
---

# EnrollmentPolicyFlags enumeration


## -description

The <b>EnrollmentPolicyFlags</b> enumeration specifies group policy flags. This enumeration type is not currently used.

## -enum-fields

### -field DisableGroupPolicyList:0x2

Ignore policy servers configured in group policy.

### -field DisableUserServerList:0x4

Ignore user configured policy servers.

