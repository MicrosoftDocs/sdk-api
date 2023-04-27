---
UID: NE:authif._RADIUS_REJECT_REASON_CODE
title: RADIUS_REJECT_REASON_CODE (authif.h)
description: The RADIUS_REJECT_REASON_CODE enumeration defines the possible RADIUS packet reject codes.
helpviewer_keywords: ["RADIUS_REJECT_REASON_CODE","RADIUS_REJECT_REASON_CODE enumeration [Network Policy Server]","authif/RADIUS_REJECT_REASON_CODE","authif/rrrcAccountDisabled","authif/rrrcAccountExpired","authif/rrrcAccountUnknown","authif/rrrcAuthenticationFailure","authif/rrrcUndefined","ias.radius_reject_reason_code","nps.IAS_radius_reject_reason_code","rrrcAccountDisabled","rrrcAccountExpired","rrrcAccountUnknown","rrrcAuthenticationFailure","rrrcUndefined"]
old-location: nps\IAS_radius_reject_reason_code.htm
tech.root: Nps
ms.assetid: b8db4404-40ab-4f28-96ce-43359c959546
ms.date: 12/05/2018
ms.keywords: RADIUS_REJECT_REASON_CODE, RADIUS_REJECT_REASON_CODE enumeration [Network Policy Server], authif/RADIUS_REJECT_REASON_CODE, authif/rrrcAccountDisabled, authif/rrrcAccountExpired, authif/rrrcAccountUnknown, authif/rrrcAuthenticationFailure, authif/rrrcUndefined, ias.radius_reject_reason_code, nps.IAS_radius_reject_reason_code, rrrcAccountDisabled, rrrcAccountExpired, rrrcAccountUnknown, rrrcAuthenticationFailure, rrrcUndefined
req.header: authif.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
req.typenames: RADIUS_REJECT_REASON_CODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RADIUS_REJECT_REASON_CODE
 - authif/_RADIUS_REJECT_REASON_CODE
 - RADIUS_REJECT_REASON_CODE
 - authif/RADIUS_REJECT_REASON_CODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AuthIf.h
api_name:
 - RADIUS_REJECT_REASON_CODE
---

# RADIUS_REJECT_REASON_CODE enumeration


## -description

<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS.</div><div> </div>The 
<b>RADIUS_REJECT_REASON_CODE</b> enumeration defines the possible RADIUS packet reject codes.

## -enum-fields

### -field rrrcUndefined:0

Reason code undefined.

### -field rrrcAccountUnknown:1

The authentication attempt is using a user name that does not correspond to any known account.

### -field rrrcAccountDisabled:2

The authentication attempt is using a user name that corresponds to an account that has been disabled by an administrator.

### -field rrrcAccountExpired:3

The authentication attempt is using a user name that corresponds to an account that has  expired, either by exceeding its natural expiration lifetime or by administrative action.

### -field rrrcAuthenticationFailure:4

The authentication process has failed; possibly due to incorrect credentials.

## -see-also

<a href="/windows/desktop/Nps/ias-about-internet-authentication-service">About NPS Extensions</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-enumerations">NPS Extensions Enumerations</a>



<a href="/windows/desktop/Nps/ias-internet-authentication-service-reference">NPS Extensions Reference</a>
