---
UID: NE:authif._RADIUS_REJECT_REASON_CODE
title: "_RADIUS_REJECT_REASON_CODE"
author: windows-sdk-content
description: The RADIUS_REJECT_REASON_CODE enumeration defines the possible RADIUS packet reject codes.
old-location: nps\IAS_radius_reject_reason_code.htm
old-project: nps
ms.assetid: b8db4404-40ab-4f28-96ce-43359c959546
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RADIUS_REJECT_REASON_CODE, RADIUS_REJECT_REASON_CODE enumeration [Network Policy Server], _RADIUS_REJECT_REASON_CODE, authif/RADIUS_REJECT_REASON_CODE, authif/rrrcAccountDisabled, authif/rrrcAccountExpired, authif/rrrcAccountUnknown, authif/rrrcAuthenticationFailure, authif/rrrcUndefined, ias.radius_reject_reason_code, nps.IAS_radius_reject_reason_code, rrrcAccountDisabled, rrrcAccountExpired, rrrcAccountUnknown, rrrcAuthenticationFailure, rrrcUndefined
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: authif.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RADIUS_REJECT_REASON_CODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - AuthIf.h
api_name:
 - RADIUS_REJECT_REASON_CODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _RADIUS_REJECT_REASON_CODE enumeration


## -description


<div class="alert"><b>Note</b>  Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.  The content of this topic applies to both IAS and NPS.</div><div> </div>The 
<b>RADIUS_REJECT_REASON_CODE</b> enumeration defines the possible RADIUS packet reject codes.


## -enum-fields




### -field rrrcUndefined

Reason code undefined.


### -field rrrcAccountUnknown

The authentication attempt is using a user name that does not correspond to any known account.


### -field rrrcAccountDisabled

The authentication attempt is using a user name that corresponds to an account that has been disabled by an administrator.


### -field rrrcAccountExpired

The authentication attempt is using a user name that corresponds to an account that has  expired, either by exceeding its natural expiration lifetime or by administrative action.


### -field rrrcAuthenticationFailure

The authentication process has failed; possibly due to incorrect credentials.


## -see-also




<a href="https://msdn.microsoft.com/3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f">About NPS Extensions</a>



<a href="https://msdn.microsoft.com/6bf9c421-f0f6-4c75-bb4d-dbe91dcb8d01">NPS Extensions Enumerations</a>



<a href="https://msdn.microsoft.com/2b7a16cb-bc64-4e81-8149-82f51c451312">NPS Extensions Reference</a>
 

 

