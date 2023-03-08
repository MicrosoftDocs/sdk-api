---
UID: NE:ntsecapi._MSV1_0_PROFILE_BUFFER_TYPE
title: MSV1_0_PROFILE_BUFFER_TYPE (ntsecapi.h)
description: Lists the kind of logon profile returned.
helpviewer_keywords: ["*PMSV1_0_PROFILE_BUFFER_TYPE","MSV1_0_PROFILE_BUFFER_TYPE","MSV1_0_PROFILE_BUFFER_TYPE enumeration [Security]","MSV1_0_PROFILE_TYPE","MSV1_0_PROFILE_TYPE enumeration [Security]","MsV1_0InteractiveProfile","MsV1_0Lm20LogonProfile","MsV1_0SmartCardProfile","PMSV1_0_PROFILE_BUFFER_TYPE","PMSV1_0_PROFILE_BUFFER_TYPE enumeration pointer [Security]","_lsa_msv1_0_profile_buffer_type","ntsecapi/MSV1_0_PROFILE_BUFFER_TYPE","ntsecapi/MsV1_0InteractiveProfile","ntsecapi/MsV1_0Lm20LogonProfile","ntsecapi/MsV1_0SmartCardProfile","ntsecapi/PMSV1_0_PROFILE_BUFFER_TYPE","security.msv1_0_profile_buffer_type"]
old-location: security\msv1_0_profile_buffer_type.htm
tech.root: security
ms.assetid: c8fe967a-e172-4200-ab15-daebf441c689
ms.date: 12/05/2018
ms.keywords: '*PMSV1_0_PROFILE_BUFFER_TYPE, MSV1_0_PROFILE_BUFFER_TYPE, MSV1_0_PROFILE_BUFFER_TYPE enumeration [Security], MSV1_0_PROFILE_TYPE, MSV1_0_PROFILE_TYPE enumeration [Security], MsV1_0InteractiveProfile, MsV1_0Lm20LogonProfile, MsV1_0SmartCardProfile, PMSV1_0_PROFILE_BUFFER_TYPE, PMSV1_0_PROFILE_BUFFER_TYPE enumeration pointer [Security], _lsa_msv1_0_profile_buffer_type, ntsecapi/MSV1_0_PROFILE_BUFFER_TYPE, ntsecapi/MsV1_0InteractiveProfile, ntsecapi/MsV1_0Lm20LogonProfile, ntsecapi/MsV1_0SmartCardProfile, ntsecapi/PMSV1_0_PROFILE_BUFFER_TYPE, security.msv1_0_profile_buffer_type'
req.header: ntsecapi.h
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
req.typenames: MSV1_0_PROFILE_BUFFER_TYPE, *PMSV1_0_PROFILE_BUFFER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MSV1_0_PROFILE_BUFFER_TYPE
 - ntsecapi/_MSV1_0_PROFILE_BUFFER_TYPE
 - PMSV1_0_PROFILE_BUFFER_TYPE
 - ntsecapi/PMSV1_0_PROFILE_BUFFER_TYPE
 - MSV1_0_PROFILE_BUFFER_TYPE
 - ntsecapi/MSV1_0_PROFILE_BUFFER_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - MSV1_0_PROFILE_TYPE
---

# MSV1_0_PROFILE_BUFFER_TYPE enumeration


## -description

The <b>MSV1_0_PROFILE_BUFFER_TYPE</b> enumeration lists the kind of logon profile returned.

## -enum-fields

### -field MsV1_0InteractiveProfile:2

The profile describes an interactive <a href="/windows/desktop/SecGloss/l-gly">logon session</a>.

### -field MsV1_0Lm20LogonProfile

The profile describes a network logon session.

### -field MsV1_0SmartCardProfile

The profile describes a <a href="/windows/desktop/SecGloss/s-gly">smart card</a> logon session.
