---
UID: NS:ntsecapi._KERB_TICKET_PROFILE
title: "_KERB_TICKET_PROFILE"
author: windows-sdk-content
description: The KERB_TICKET_PROFILE structure contains information about an interactive logon profile. This structure is returned by LsaLogonUser.
old-location: security\kerb_ticket_profile.htm
tech.root: secauthn
ms.assetid: 9db0f9ac-b469-4e62-a735-ca3c56086009
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: "*PKERB_TICKET_PROFILE, KERB_TICKET_PROFILE, KERB_TICKET_PROFILE structure [Security], PKERB_TICKET_PROFILE, PKERB_TICKET_PROFILE structure pointer [Security], _KERB_TICKET_PROFILE, _lsa_kerb_ticket_profile, ntsecapi/KERB_TICKET_PROFILE, ntsecapi/PKERB_TICKET_PROFILE, security.kerb_ticket_profile"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - KERB_TICKET_PROFILE
product: Windows
targetos: Windows
req.typenames: KERB_TICKET_PROFILE, *PKERB_TICKET_PROFILE
req.redist: 
---

# _KERB_TICKET_PROFILE structure


## -description


The <b>KERB_TICKET_PROFILE</b> structure contains information about an interactive logon profile.
			

This structure is returned by 
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>.


## -struct-fields




### -field Profile


<a href="https://msdn.microsoft.com/8e9dd04b-8155-4f85-be00-ff9d8297deaa">KERB_INTERACTIVE_PROFILE</a> structure containing logon information.


### -field SessionKey


<a href="https://msdn.microsoft.com/ac7ea61c-b1e0-4dc0-931e-81bb6fd74888">KERB_CRYPTO_KEY</a> structure containing the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session key</a> for the Kerberos ticket.

