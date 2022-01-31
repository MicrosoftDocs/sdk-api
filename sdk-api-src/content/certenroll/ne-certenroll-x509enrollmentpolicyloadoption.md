---
UID: NE:certenroll.X509EnrollmentPolicyLoadOption
title: X509EnrollmentPolicyLoadOption (certenroll.h)
description: Is used by the LoadPolicy method on the IX509EnrollmentPolicyServer interface to specify how to retrieve policy from the policy server.
helpviewer_keywords: ["LoadOptionCacheOnly","LoadOptionDefault","LoadOptionRegisterForADChanges","LoadOptionReload","X509EnrollmentPolicyLoadOption","X509EnrollmentPolicyLoadOption enumeration [Security]","certenroll/LoadOptionCacheOnly","certenroll/LoadOptionDefault","certenroll/LoadOptionRegisterForADChanges","certenroll/LoadOptionReload","certenroll/X509EnrollmentPolicyLoadOption","security.x509enrollmentpolicyloadoption"]
old-location: security\x509enrollmentpolicyloadoption.htm
tech.root: security
ms.assetid: 94adcffd-b4fe-4bd9-912c-9e8d5e5fdb5b
ms.date: 12/05/2018
ms.keywords: LoadOptionCacheOnly, LoadOptionDefault, LoadOptionRegisterForADChanges, LoadOptionReload, X509EnrollmentPolicyLoadOption, X509EnrollmentPolicyLoadOption enumeration [Security], certenroll/LoadOptionCacheOnly, certenroll/LoadOptionDefault, certenroll/LoadOptionRegisterForADChanges, certenroll/LoadOptionReload, certenroll/X509EnrollmentPolicyLoadOption, security.x509enrollmentpolicyloadoption
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
req.typenames: X509EnrollmentPolicyLoadOption
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X509EnrollmentPolicyLoadOption
 - certenroll/X509EnrollmentPolicyLoadOption
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
 - X509EnrollmentPolicyLoadOption
---

# X509EnrollmentPolicyLoadOption enumeration


## -description

The <b>X509EnrollmentPolicyLoadOption</b> enumeration is used by the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-loadpolicy">LoadPolicy</a> method on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a> interface to specify how to retrieve policy from the policy server.

## -enum-fields

### -field LoadOptionDefault:0

Reload if the cache has expired.

### -field LoadOptionCacheOnly:1

Always load from the cache even if it has expired.

### -field LoadOptionReload:2

Always reload.

### -field LoadOptionRegisterForADChanges:4

Registers a thread to update a sequence number if there are changes to the template or the certification authority container. This value applies only to an Active Directory policy server.

## -see-also

<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-loadpolicy">LoadPolicy</a>
