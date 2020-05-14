---
UID: NE:ntsecapi._KERB_PROFILE_BUFFER_TYPE
title: KERB_PROFILE_BUFFER_TYPE (ntsecapi.h)
description: Lists the type of logon profile returned.helpviewer_keywords: ["*PKERB_PROFILE_BUFFER_TYPE","KERB_PROFILE_BUFFER_TYPE","KERB_PROFILE_BUFFER_TYPE enumeration [Security]","KerbInteractiveProfile","KerbTicketProfile","PKERB_PROFILE_BUFFER_TYPE","PKERB_PROFILE_BUFFER_TYPE enumeration pointer [Security]","_lsa_kerb_profile_buffer_type","ntsecapi/KERB_PROFILE_BUFFER_TYPE","ntsecapi/KerbInteractiveProfile","ntsecapi/KerbTicketProfile","ntsecapi/PKERB_PROFILE_BUFFER_TYPE","security.kerb_profile_buffer_type"]
old-location: security\kerb_profile_buffer_type.htm
tech.root: SecAuthN
ms.assetid: c590b6fd-c241-4ff8-9475-c8af7de7b431
ms.date: 12/05/2018
ms.keywords: '*PKERB_PROFILE_BUFFER_TYPE, KERB_PROFILE_BUFFER_TYPE, KERB_PROFILE_BUFFER_TYPE enumeration [Security], KerbInteractiveProfile, KerbTicketProfile, PKERB_PROFILE_BUFFER_TYPE, PKERB_PROFILE_BUFFER_TYPE enumeration pointer [Security], _lsa_kerb_profile_buffer_type, ntsecapi/KERB_PROFILE_BUFFER_TYPE, ntsecapi/KerbInteractiveProfile, ntsecapi/KerbTicketProfile, ntsecapi/PKERB_PROFILE_BUFFER_TYPE, security.kerb_profile_buffer_type'
f1_keywords:
- ntsecapi/KERB_PROFILE_BUFFER_TYPE
dev_langs:
- c++
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
- KERB_PROFILE_BUFFER_TYPE
targetos: Windows
req.typenames: KERB_PROFILE_BUFFER_TYPE, *PKERB_PROFILE_BUFFER_TYPE
req.redist: 
ms.custom: 19H1
---

# KERB_PROFILE_BUFFER_TYPE enumeration


## -description


The <b>KERB_PROFILE_BUFFER_TYPE</b> enumeration lists the type of logon profile returned.


## -enum-fields




### -field KerbInteractiveProfile

The buffer contains information about an interactive <a href="https://docs.microsoft.com/windows/desktop/SecGloss/l-gly">logon session</a>.


### -field KerbSmartCardProfile


### -field KerbTicketProfile

The buffer contains information about a Kerberos logon session.

