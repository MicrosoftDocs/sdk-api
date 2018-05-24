---
UID: NS:ntsecapi._MSV1_0_SUBAUTH_RESPONSE
title: "_MSV1_0_SUBAUTH_RESPONSE"
author: windows-driver-content
description: Contains the response from a subauthentication package.
old-location: security\msv1_0_subauth_response.htm
old-project: SecAuthN
ms.assetid: 62808fba-6e10-4f3b-a705-6958fc4fe480
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: "*PMSV1_0_SUBAUTH_RESPONSE, MSV1_0_SUBAUTH_RESPONSE, MSV1_0_SUBAUTH_RESPONSE structure [Security], PMSV1_0_SUBAUTH_RESPONSE, PMSV1_0_SUBAUTH_RESPONSE structure pointer [Security], _MSV1_0_SUBAUTH_RESPONSE, _lsa_msv1_0_subauth_response, ntsecapi/MSV1_0_SUBAUTH_RESPONSE, ntsecapi/PMSV1_0_SUBAUTH_RESPONSE, security.msv1_0_subauth_response"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MSV1_0_SUBAUTH_RESPONSE, *PMSV1_0_SUBAUTH_RESPONSE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	MSV1_0_SUBAUTH_RESPONSE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# _MSV1_0_SUBAUTH_RESPONSE structure


## -description


The <b>MSV1_0_SUBAUTH_RESPONSE</b> structure contains the response from a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subauthentication package</a>.

It is used by 
<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a>.


## -struct-fields




### -field MessageType


<a href="https://msdn.microsoft.com/9498558c-8daf-4dfb-aa1c-0598154ca8c4">MSV1_0_PROTOCOL_MESSAGE_TYPE</a> value identifying the type of request being made. This member must be set to <b>MsV1_0SubAuth</b>.


### -field SubAuthInfoLength

Indicates the length, in bytes, of the buffer returned by <b>SubAuthReturnBuffer</b>.


### -field SubAuthReturnBuffer

Contains the subauthentication package response. The format and content of this buffer is specific to the subauthentication package. For more information, see the documentation for specific subauthentication packages.

