---
UID: NS:iketypes.IKEEXT_EM_POLICY0_
title: IKEEXT_EM_POLICY0 (iketypes.h)
description: Is used to store AuthIP's extended mode negotiation policy. (IKEEXT_EM_POLICY0)
helpviewer_keywords: ["IKEEXT_EM_POLICY0","IKEEXT_EM_POLICY0 structure [Filtering]","fwp.ikeext_em_policy0","iketypes/IKEEXT_EM_POLICY0"]
old-location: fwp\ikeext_em_policy0.htm
tech.root: fwp
ms.assetid: 954a2bb8-eb54-4f41-8a0c-3f2af1190f57
ms.date: 12/05/2018
ms.keywords: IKEEXT_EM_POLICY0, IKEEXT_EM_POLICY0 structure [Filtering], fwp.ikeext_em_policy0, iketypes/IKEEXT_EM_POLICY0
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: IKEEXT_EM_POLICY0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_EM_POLICY0_
 - iketypes/IKEEXT_EM_POLICY0_
 - IKEEXT_EM_POLICY0
 - iketypes/IKEEXT_EM_POLICY0
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
 - IKEEXT_EM_POLICY0
---

# IKEEXT_EM_POLICY0 structure


## -description

The <b>IKEEXT_EM_POLICY0</b> structure is used to store AuthIP's extended mode negotiation policy.
[IKEEXT_EM_POLICY2](/windows/desktop/api/iketypes/ns-iketypes-ikeext_em_policy2) is available.</div><div> </div>

## -struct-fields

### -field numAuthenticationMethods

Number of authentication methods in the array.

### -field authenticationMethods

size_is(numAuthenticationMethods)

Array of acceptable authentication methods as specified by [IKEEXT_AUTHENTICATION_METHOD0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_authentication_method0).

### -field initiatorImpersonationType

Type of impersonation.

See <a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_impersonation_type">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a> for more information.

## -remarks

Applies only to AuthIP.

## -see-also

<a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_impersonation_type">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a>



[IKEEXT_AUTHENTICATION_METHOD0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_authentication_method0)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
