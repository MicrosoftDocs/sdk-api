---
UID: NS:ntsecapi._MSV1_0_SUBAUTH_RESPONSE
title: MSV1_0_SUBAUTH_RESPONSE (ntsecapi.h)
description: Contains the response from a subauthentication package.
helpviewer_keywords: ["*PMSV1_0_SUBAUTH_RESPONSE","MSV1_0_SUBAUTH_RESPONSE","MSV1_0_SUBAUTH_RESPONSE structure [Security]","PMSV1_0_SUBAUTH_RESPONSE","PMSV1_0_SUBAUTH_RESPONSE structure pointer [Security]","_lsa_msv1_0_subauth_response","ntsecapi/MSV1_0_SUBAUTH_RESPONSE","ntsecapi/PMSV1_0_SUBAUTH_RESPONSE","security.msv1_0_subauth_response"]
old-location: security\msv1_0_subauth_response.htm
tech.root: security
ms.assetid: 62808fba-6e10-4f3b-a705-6958fc4fe480
ms.date: 12/05/2018
ms.keywords: '*PMSV1_0_SUBAUTH_RESPONSE, MSV1_0_SUBAUTH_RESPONSE, MSV1_0_SUBAUTH_RESPONSE structure [Security], PMSV1_0_SUBAUTH_RESPONSE, PMSV1_0_SUBAUTH_RESPONSE structure pointer [Security], _lsa_msv1_0_subauth_response, ntsecapi/MSV1_0_SUBAUTH_RESPONSE, ntsecapi/PMSV1_0_SUBAUTH_RESPONSE, security.msv1_0_subauth_response'
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
req.typenames: MSV1_0_SUBAUTH_RESPONSE, *PMSV1_0_SUBAUTH_RESPONSE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MSV1_0_SUBAUTH_RESPONSE
 - ntsecapi/_MSV1_0_SUBAUTH_RESPONSE
 - PMSV1_0_SUBAUTH_RESPONSE
 - ntsecapi/PMSV1_0_SUBAUTH_RESPONSE
 - MSV1_0_SUBAUTH_RESPONSE
 - ntsecapi/MSV1_0_SUBAUTH_RESPONSE
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
 - MSV1_0_SUBAUTH_RESPONSE
---

# MSV1_0_SUBAUTH_RESPONSE structure


## -description

The <b>MSV1_0_SUBAUTH_RESPONSE</b> structure contains the response from a <a href="/windows/desktop/SecGloss/s-gly">subauthentication package</a>.

It is used by 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>.

## -struct-fields

### -field MessageType

<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-msv1_0_protocol_message_type">MSV1_0_PROTOCOL_MESSAGE_TYPE</a> value identifying the type of request being made. This member must be set to <b>MsV1_0SubAuth</b>.

### -field SubAuthInfoLength

Indicates the length, in bytes, of the buffer returned by <b>SubAuthReturnBuffer</b>.

### -field SubAuthReturnBuffer

Contains the subauthentication package response. The format and content of this buffer is specific to the subauthentication package. For more information, see the documentation for specific subauthentication packages.