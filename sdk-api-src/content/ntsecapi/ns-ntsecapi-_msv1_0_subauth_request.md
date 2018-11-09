---
UID: NS:ntsecapi._MSV1_0_SUBAUTH_REQUEST
title: "_MSV1_0_SUBAUTH_REQUEST"
author: windows-sdk-content
description: Contains information to pass to an subauthentication package.
old-location: security\msv1_0_subauth_request.htm
tech.root: secauthn
ms.assetid: 5a408c0a-56d4-48f6-8289-6f203ef998df
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "*PMSV1_0_SUBAUTH_REQUEST, MSV1_0_SUBAUTH_REQUEST, MSV1_0_SUBAUTH_REQUEST structure [Security], PMSV1_0_SUBAUTH_REQUEST, PMSV1_0_SUBAUTH_REQUEST structure pointer [Security], _MSV1_0_SUBAUTH_REQUEST, _lsa_msv1_0_subauth_request, ntsecapi/MSV1_0_SUBAUTH_REQUEST, ntsecapi/PMSV1_0_SUBAUTH_REQUEST, security.msv1_0_subauth_request"
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
 - MSV1_0_SUBAUTH_REQUEST
product: Windows
targetos: Windows
req.typenames: MSV1_0_SUBAUTH_REQUEST, *PMSV1_0_SUBAUTH_REQUEST
req.redist: 
---

# _MSV1_0_SUBAUTH_REQUEST structure


## -description


The <b>MSV1_0_SUBAUTH_REQUEST</b> structure contains information to pass to an <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subauthentication package</a>.

It is used by 
<a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a>.


## -struct-fields




### -field MessageType


<a href="https://msdn.microsoft.com/9498558c-8daf-4dfb-aa1c-0598154ca8c4">MSV1_0_PROTOCOL_MESSAGE_TYPE</a> value identifying the type of request being made. This member should be set to <b>MsV1_0SubAuth</b> for local subauthentication and <b>MsV1_0GenericPassthrough</b> for subauthentication on the domain controller.


### -field SubAuthPackageId

Contains a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subauthentication package</a> identifier. The value of subauthentication package identifiers is established by the creator of the subauthentication package.


### -field SubAuthInfoLength

Indicates the length, in bytes, of the buffer passed to the subauthentication package in <b>SubAuthSubmitBuffer</b>.


### -field SubAuthSubmitBuffer

Containing the data to pass to the subauthentication package. The format and content of this data is specific to the subauthentication package. For more information, see the documentation for specific subauthentication packages.

