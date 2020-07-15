---
UID: NS:ntsecapi._KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE
title: KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE (ntsecapi.h)
description: Contains the results of querying for the extended policies of the specified domain.
helpviewer_keywords: ["*PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE","KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE","KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE structure [Security]","KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE_FLAG_DAC_DISABLED","PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE","PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE structure pointer [Security]","ntsecapi/KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE","ntsecapi/PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE","security.kerb_query_domain_extended_policies_response"]
old-location: security\kerb_query_domain_extended_policies_response.htm
tech.root: SecAuthN
ms.assetid: 4BFF08D8-9D5E-4041-9DF6-AAE44292C135
ms.date: 12/05/2018
ms.keywords: '*PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE, KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE, KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE structure [Security], KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE_FLAG_DAC_DISABLED, PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE, PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE structure pointer [Security], ntsecapi/KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE, ntsecapi/PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE, security.kerb_query_domain_extended_policies_response'
f1_keywords:
- ntsecapi/KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE
dev_langs:
- c++
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
targetos: Windows
req.typenames: KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE, *PKERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE
req.redist: 
ms.custom: 19H1
---

# KERB_QUERY_DOMAIN_EXTENDED_POLICIES_RESPONSE structure


## -description


Contains the results of querying for the extended policies of the specified domain. You must have the <b>SeTcbPrivilege</b> privilege set.


## -struct-fields




### -field MessageType

A 
						value of the <a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/ne-ntsecapi-kerb_protocol_message_type">KERB_PROTOCOL_MESSAGE_TYPE</a> enumeration that lists the types of messages that can be sent to the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/k-gly">Kerberos</a> authentication package by calling 
the <a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage">LsaCallAuthenticationPackage</a> function. This member must be set to <b>KerbQueryDomainExtendedPoliciesMessage</b>.


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

Flags that represent the requirements. These flags are returned from the <a href="https://docs.microsoft.com/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> function.

