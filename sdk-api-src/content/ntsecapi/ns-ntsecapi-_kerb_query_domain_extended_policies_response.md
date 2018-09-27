---
UID: NS:ntsecapi._KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE
title: "_KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE"
author: windows-sdk-content
description: Contains the results of querying for the extended policies of the specified domain.
old-location: security\kerb_query_domain_extended_policies_response.htm
tech.root: secauthn
ms.assetid: 4BFF08D8-9D5E-4041-9DF6-AAE44292C135
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE, KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE, KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE structure [Security], KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE_FLAG_DAC_DISABLED, PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE, PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE structure pointer [Security], _KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE, ntsecapi/KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE, ntsecapi/PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE, security.kerb_query_domain_extended_policies_response"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE
product: Windows
targetos: Windows
req.typenames: KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE, *PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE
req.redist: 
---

# _KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE structure


## -description


Contains the results of querying for the extended policies of the specified domain. You must have the <b>SeTcbPrivilege</b> privilege set.


## -struct-fields




### -field MessageType

A 
						value of the <a href="https://msdn.microsoft.com/8ad183d2-3fe8-4f52-bfa4-16f2a711f0c3">KERB_PROTOCOL_MESSAGE_TYPE</a> enumeration that lists the types of messages that can be sent to the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">Kerberos</a> authentication package by calling 
the <a href="https://msdn.microsoft.com/b891fa60-28b3-4819-9a92-e4524677fa4f">LsaCallAuthenticationPackage</a> function. This member must be set to <b>KerbQueryDomainExtendedPoliciesMessage</b>.


### -field Flags

Contains flags used for the extended policies.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE_FLAG_DAC_DISABLED"></a><a id="kerb_query_domain_extended_policies_response_flag_dac_disabled"></a><dl>
<dt><b>KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE_FLAG_DAC_DISABLED</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The Dynamic Access Control (DAC) is disabled so you can't get the extended policies.

</td>
</tr>
</table>
 


### -field ExtendedPolicies

The 	name of the domain that you are querying for the extended policies.


### -field DsFlags

Flags that represent the requirements. These flags are returned from the <a href="https://msdn.microsoft.com/da8b2983-5e45-40b0-b552-c9b3a1d8ae94">DsGetDcName</a> function.

