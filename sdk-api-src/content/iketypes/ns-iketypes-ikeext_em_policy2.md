---
UID: NS:iketypes.IKEEXT_EM_POLICY2_
title: IKEEXT_EM_POLICY2 (iketypes.h)
description: Is used to store AuthIP's extended mode negotiation policy. (IKEEXT_EM_POLICY2)
helpviewer_keywords: ["IKEEXT_EM_POLICY2","IKEEXT_EM_POLICY2 structure [Filtering]","fwp.ikeext_em_policy2","iketypes/IKEEXT_EM_POLICY2"]
old-location: fwp\ikeext_em_policy2.htm
tech.root: fwp
ms.assetid: 01e3122b-812f-4c01-a514-dc0d513de822
ms.date: 12/05/2018
ms.keywords: IKEEXT_EM_POLICY2, IKEEXT_EM_POLICY2 structure [Filtering], fwp.ikeext_em_policy2, iketypes/IKEEXT_EM_POLICY2
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: IKEEXT_EM_POLICY2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_EM_POLICY2_
 - iketypes/IKEEXT_EM_POLICY2_
 - IKEEXT_EM_POLICY2
 - iketypes/IKEEXT_EM_POLICY2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - iketypes.h
api_name:
 - IKEEXT_EM_POLICY2
---

# IKEEXT_EM_POLICY2 structure


## -description

The <b>IKEEXT_EM_POLICY2</b> structure is used to store AuthIP's extended mode negotiation policy.
[IKEEXT_EM_POLICY0](/windows/desktop/api/iketypes/ns-iketypes-ikeext_em_policy0)  is available.</div><div> </div>

## -struct-fields

### -field numAuthenticationMethods

Type: <b>UINT32</b>

 Number of authentication methods in the array.

### -field authenticationMethods

Type: [IKEEXT_AUTHENTICATION_METHOD2](/windows/desktop/api/iketypes/ns-iketypes-ikeext_authentication_method2)*</b>

size_is(numAuthenticationMethods)

Array of acceptable authentication methods.

### -field initiatorImpersonationType

Type: <b><a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_impersonation_type">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a></b>

Type of impersonation.

## -see-also

<a href="/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_impersonation_type">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a>



[IKEEXT_AUTHENTICATION_METHOD2](/windows/desktop/api/iketypes/ns-iketypes-ikeext_authentication_method2)



<a href="/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
