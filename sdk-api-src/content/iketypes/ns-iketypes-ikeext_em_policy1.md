---
UID: NS:iketypes.IKEEXT_EM_POLICY1_
title: IKEEXT_EM_POLICY1 (iketypes.h)
description: Is used to store AuthIP's extended mode negotiation policy. (IKEEXT_EM_POLICY1)
helpviewer_keywords: ["IKEEXT_EM_POLICY1","IKEEXT_EM_POLICY1 structure [Filtering]","fwp.ikeext_em_policy1","iketypes/IKEEXT_EM_POLICY1"]
old-location: fwp\ikeext_em_policy1.htm
tech.root: fwp
ms.assetid: dae56d71-31e0-4746-8bfb-4ade3705278f
ms.date: 12/05/2018
ms.keywords: IKEEXT_EM_POLICY1, IKEEXT_EM_POLICY1 structure [Filtering], fwp.ikeext_em_policy1, iketypes/IKEEXT_EM_POLICY1
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: IKEEXT_EM_POLICY1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_EM_POLICY1_
 - iketypes/IKEEXT_EM_POLICY1_
 - IKEEXT_EM_POLICY1
 - iketypes/IKEEXT_EM_POLICY1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_EM_POLICY1
---

# IKEEXT_EM_POLICY1 structure


## -description

The <b>IKEEXT_EM_POLICY1</b> structure is used to store AuthIP's extended mode negotiation policy.
[IKEEXT_EM_POLICY2](/windows/desktop/api/iketypes/ns-iketypes-ikeext_em_policy2) is available. For Windows Vista, [IKEEXT_EM_POLICY0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_em_policy0) is available.</div><div> </div>

## -struct-fields

### -field numAuthenticationMethods

Number of authentication methods in the array.

### -field authenticationMethods

size_is(numAuthenticationMethods)

Array of acceptable authentication methods as specified by [IKEEXT_AUTHENTICATION_METHOD1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_authentication_method1).

### -field initiatorImpersonationType

Type of impersonation.

See <a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_impersonation_type">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a> for more information.

## -remarks

Applies only to AuthIP.

## -see-also

<a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_impersonation_type">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a>



[IKEEXT_AUTHENTICATION_METHOD1](/windows/desktop/api/iketypes/ns-iketypes-ikeext_authentication_method1)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
