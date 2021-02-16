---
UID: NE:accctrl._MULTIPLE_TRUSTEE_OPERATION
title: MULTIPLE_TRUSTEE_OPERATION (accctrl.h)
description: Contains values that indicate whether a TRUSTEE structure is an impersonation trustee.
helpviewer_keywords: ["MULTIPLE_TRUSTEE_OPERATION","MULTIPLE_TRUSTEE_OPERATION enumeration [Security]","NO_MULTIPLE_TRUSTEE","TRUSTEE_IS_IMPERSONATE","_win32_multiple_trustee_operation_str","accctrl/MULTIPLE_TRUSTEE_OPERATION","accctrl/NO_MULTIPLE_TRUSTEE","accctrl/TRUSTEE_IS_IMPERSONATE","security.multiple_trustee_operation"]
old-location: security\multiple_trustee_operation.htm
tech.root: security
ms.assetid: 00b00678-5c87-4aa9-8232-5f0f1cb48e24
ms.date: 12/05/2018
ms.keywords: MULTIPLE_TRUSTEE_OPERATION, MULTIPLE_TRUSTEE_OPERATION enumeration [Security], NO_MULTIPLE_TRUSTEE, TRUSTEE_IS_IMPERSONATE, _win32_multiple_trustee_operation_str, accctrl/MULTIPLE_TRUSTEE_OPERATION, accctrl/NO_MULTIPLE_TRUSTEE, accctrl/TRUSTEE_IS_IMPERSONATE, security.multiple_trustee_operation
req.header: accctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: MULTIPLE_TRUSTEE_OPERATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MULTIPLE_TRUSTEE_OPERATION
 - accctrl/_MULTIPLE_TRUSTEE_OPERATION
 - MULTIPLE_TRUSTEE_OPERATION
 - accctrl/MULTIPLE_TRUSTEE_OPERATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AccCtrl.h
api_name:
 - MULTIPLE_TRUSTEE_OPERATION
---

# MULTIPLE_TRUSTEE_OPERATION enumeration


## -description

The <b>MULTIPLE_TRUSTEE_OPERATION</b> enumeration contains values that indicate whether a 
<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure is an impersonation trustee.

## -enum-fields

### -field NO_MULTIPLE_TRUSTEE

The trustee is not an impersonation trustee.

### -field TRUSTEE_IS_IMPERSONATE

The trustee is an impersonation trustee. The <b>pMultipleTrustee</b> member of the <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure points to a trustee for a server that can impersonate the client trustee.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-enumerations">Authorization Enumerations</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a>