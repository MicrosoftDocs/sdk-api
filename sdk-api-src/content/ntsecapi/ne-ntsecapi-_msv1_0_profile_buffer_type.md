---
UID: NE:ntsecapi._MSV1_0_PROFILE_BUFFER_TYPE
title: "_MSV1_0_PROFILE_BUFFER_TYPE"
author: windows-sdk-content
description: Lists the kind of logon profile returned.
old-location: security\msv1_0_profile_buffer_type.htm
old-project: secauthn
ms.assetid: c8fe967a-e172-4200-ab15-daebf441c689
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: "*PMSV1_0_PROFILE_BUFFER_TYPE, MSV1_0_PROFILE_BUFFER_TYPE, MSV1_0_PROFILE_BUFFER_TYPE enumeration [Security], MSV1_0_PROFILE_TYPE, MSV1_0_PROFILE_TYPE enumeration [Security], MsV1_0InteractiveProfile, MsV1_0Lm20LogonProfile, MsV1_0SmartCardProfile, PMSV1_0_PROFILE_BUFFER_TYPE, PMSV1_0_PROFILE_BUFFER_TYPE enumeration pointer [Security], _MSV1_0_PROFILE_BUFFER_TYPE, _lsa_msv1_0_profile_buffer_type, ntsecapi/MSV1_0_PROFILE_BUFFER_TYPE, ntsecapi/MsV1_0InteractiveProfile, ntsecapi/MsV1_0Lm20LogonProfile, ntsecapi/MsV1_0SmartCardProfile, ntsecapi/PMSV1_0_PROFILE_BUFFER_TYPE, security.msv1_0_profile_buffer_type"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ntsecapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MSV1_0_PROFILE_BUFFER_TYPE, *PMSV1_0_PROFILE_BUFFER_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - MSV1_0_PROFILE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _MSV1_0_PROFILE_BUFFER_TYPE enumeration


## -description


The <b>MSV1_0_PROFILE_BUFFER_TYPE</b> enumeration lists the kind of logon profile returned.


## -enum-fields




### -field MsV1_0InteractiveProfile

The profile describes an interactive <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a>.


### -field MsV1_0Lm20LogonProfile

The profile describes a network logon session.


### -field MsV1_0SmartCardProfile

The profile describes a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a> logon session.

