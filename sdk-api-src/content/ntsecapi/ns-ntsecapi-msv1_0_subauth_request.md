---
UID: NS:ntsecapi._MSV1_0_SUBAUTH_REQUEST
title: MSV1_0_SUBAUTH_REQUEST (ntsecapi.h)
description: Contains information to pass to a subauthentication package.
helpviewer_keywords: ["*PMSV1_0_SUBAUTH_REQUEST","MSV1_0_SUBAUTH_REQUEST","MSV1_0_SUBAUTH_REQUEST structure [Security]","PMSV1_0_SUBAUTH_REQUEST","PMSV1_0_SUBAUTH_REQUEST structure pointer [Security]","_lsa_msv1_0_subauth_request","ntsecapi/MSV1_0_SUBAUTH_REQUEST","ntsecapi/PMSV1_0_SUBAUTH_REQUEST","security.msv1_0_subauth_request"]
old-location: security\msv1_0_subauth_request.htm
tech.root: security
ms.assetid: 5a408c0a-56d4-48f6-8289-6f203ef998df
ms.date: 12/05/2018
ms.keywords: '*PMSV1_0_SUBAUTH_REQUEST, MSV1_0_SUBAUTH_REQUEST, MSV1_0_SUBAUTH_REQUEST structure [Security], PMSV1_0_SUBAUTH_REQUEST, PMSV1_0_SUBAUTH_REQUEST structure pointer [Security], _lsa_msv1_0_subauth_request, ntsecapi/MSV1_0_SUBAUTH_REQUEST, ntsecapi/PMSV1_0_SUBAUTH_REQUEST, security.msv1_0_subauth_request'
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
req.typenames: MSV1_0_SUBAUTH_REQUEST, *PMSV1_0_SUBAUTH_REQUEST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MSV1_0_SUBAUTH_REQUEST
 - ntsecapi/_MSV1_0_SUBAUTH_REQUEST
 - PMSV1_0_SUBAUTH_REQUEST
 - ntsecapi/PMSV1_0_SUBAUTH_REQUEST
 - MSV1_0_SUBAUTH_REQUEST
 - ntsecapi/MSV1_0_SUBAUTH_REQUEST
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
 - MSV1_0_SUBAUTH_REQUEST
---

# MSV1_0_SUBAUTH_REQUEST structure


## -description

The <b>MSV1_0_SUBAUTH_REQUEST</b> structure contains information to pass to a <a href="/windows/desktop/SecGloss/s-gly">subauthentication package</a>.

It is used by 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a>.

## -struct-fields

### -field MessageType

<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-msv1_0_protocol_message_type">MSV1_0_PROTOCOL_MESSAGE_TYPE</a> value identifying the type of request being made. This member should be set to <b>MsV1_0SubAuth</b> for local subauthentication and <b>MsV1_0GenericPassthrough</b> for subauthentication on the domain controller.

### -field SubAuthPackageId

Contains a <a href="/windows/desktop/SecGloss/s-gly">subauthentication package</a> identifier. The value of subauthentication package identifiers is established by the creator of the subauthentication package.

### -field SubAuthInfoLength

Indicates the length, in bytes, of the buffer passed to the subauthentication package in <b>SubAuthSubmitBuffer</b>.

### -field SubAuthSubmitBuffer

Containing the data to pass to the subauthentication package. The format and content of this data is specific to the subauthentication package. For more information, see the documentation for specific subauthentication packages.