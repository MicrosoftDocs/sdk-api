---
UID: NS:ntsecapi._KERB_SMART_CARD_LOGON
title: KERB_SMART_CARD_LOGON
author: windows-sdk-content
description: Contains information about a smart card logon session.
old-location: security\kerb_smart_card_logon.htm
tech.root: secauthn
ms.assetid: 1a154034-6a2d-46be-9fb6-7c7d425d12f6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PKERB_SMART_CARD_LOGON, KERB_SMART_CARD_LOGON, KERB_SMART_CARD_LOGON structure [Security], PKERB_SMART_CARD_LOGON, PKERB_SMART_CARD_LOGON structure pointer [Security], ntsecapi/KERB_SMART_CARD_LOGON, ntsecapi/PKERB_SMART_CARD_LOGON, security.kerb_smart_card_logon"
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
 - KERB_SMART_CARD_LOGON
product: Windows
targetos: Windows
req.typenames: KERB_SMART_CARD_LOGON, *PKERB_SMART_CARD_LOGON
req.redist: 
---

# KERB_SMART_CARD_LOGON structure


## -description


The <b>KERB_SMART_CARD_LOGON</b> structure contains information about a smart card <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a>.

It is used by 
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a> with the Kerberos security package using LOGON32_PROVIDER_WINNT50 or LOGON32_PROVIDER_DEFAULT.


## -struct-fields




### -field MessageType


<a href="https://msdn.microsoft.com/500bee53-638b-4782-b42d-1df158396fb6">KERB_LOGON_SUBMIT_TYPE</a> value identifying the type of logon request being made. This member must be set to <b>KerbInteractiveLogon</b>.


### -field Pin


<a href="https://msdn.microsoft.com/4687d63a-4e58-4181-a48f-2724e5015e77">UNICODE_STRING</a> that specifies the PIN associated with the smart card.


### -field CspDataLength

The length, in characters, of the <b>CspData</b> member.


### -field CspData

A pointer to a <b>KERB_SMARTCARD_CSP_INFO</b> structure that contains information about the smart card cryptographic service provider (CSP) or a pointer to a marshaled <b>KERB_CERTIFICATE_INFO</b> structure when updating certificate credentials.

