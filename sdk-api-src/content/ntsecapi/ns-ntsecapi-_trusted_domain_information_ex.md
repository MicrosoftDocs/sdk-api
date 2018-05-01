---
UID: NS:ntsecapi._TRUSTED_DOMAIN_INFORMATION_EX
title: "_TRUSTED_DOMAIN_INFORMATION_EX"
author: windows-driver-content
description: Used to retrieve extended information about a trusted domain.
old-location: security\trusted_domain_information_ex.htm
old-project: SecMgmt
ms.assetid: acf9a2b5-f301-4e6a-a515-df338658ad56
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: "*PTRUSTED_DOMAIN_INFORMATION_EX, 0x00100000 to 0xFFF00000, 0x5 - 0x000FFFFF, PTRUSTED_DOMAIN_INFORMATION_EX, PTRUSTED_DOMAIN_INFORMATION_EX structure pointer [Security], TRUSTED_DOMAIN_INFORMATION_EX, TRUSTED_DOMAIN_INFORMATION_EX structure [Security], TRUST_ATTRIBUTE_CROSS_ORGANIZATION, TRUST_ATTRIBUTE_FILTER_SIDS, TRUST_ATTRIBUTE_FOREST_TRANSITIVE, TRUST_ATTRIBUTE_NON_TRANSITIVE, TRUST_ATTRIBUTE_TREAT_AS_EXTERNAL, TRUST_ATTRIBUTE_UPLEVEL_ONLY, TRUST_ATTRIBUTE_WITHIN_FOREST, TRUST_DIRECTION_BIDIRECTIONAL, TRUST_DIRECTION_DISABLED, TRUST_DIRECTION_INBOUND, TRUST_DIRECTION_OUTBOUND, TRUST_TYPE_DCE, TRUST_TYPE_DOWNLEVEL, TRUST_TYPE_MIT, TRUST_TYPE_UPLEVEL, _TRUSTED_DOMAIN_INFORMATION_EX, _lsa_trusted_domain_information_ex, ntsecapi/PTRUSTED_DOMAIN_INFORMATION_EX, ntsecapi/TRUSTED_DOMAIN_INFORMATION_EX, security.trusted_domain_information_ex"
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
req.typenames: TRUSTED_DOMAIN_INFORMATION_EX, *PTRUSTED_DOMAIN_INFORMATION_EX
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ntsecapi.h
api_name:
-	TRUSTED_DOMAIN_INFORMATION_EX
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _TRUSTED_DOMAIN_INFORMATION_EX structure


## -description


The <b>TRUSTED_DOMAIN_INFORMATION_EX</b> structure is used to retrieve extended information about a trusted domain. The 
<a href="https://msdn.microsoft.com/62925515-a6f3-4b5f-bf97-edb968af19a3">LsaQueryTrustedDomainInfo</a> function uses this structure when its <i>InformationClass</i> parameter is set to TrustedDomainInformationEx.


## -struct-fields




### -field Name

An 
<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that contains the name of the trusted domain. This is the DNS domain name.  For non-Microsoft trusted domains, this is the identifying name of the domain.


### -field FlatName

An <a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a> structure that contains the flat name of the trusted domain. For non-Microsoft trusted domains, this is the identifying name of the domain or it is <b>NULL</b>.


### -field Sid

Pointer to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) of the trusted domain. For non-Microsoft trusted domains, this member can be <b>NULL</b>.


### -field TrustDirection

A value that indicates the direction of the trust. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUST_DIRECTION_DISABLED"></a><a id="trust_direction_disabled"></a><dl>
<dt><b>TRUST_DIRECTION_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The trust relationship exists, but it has been disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUST_DIRECTION_INBOUND"></a><a id="trust_direction_inbound"></a><dl>
<dt><b>TRUST_DIRECTION_INBOUND</b></dt>
</dl>
</td>
<td width="60%">
The trusted domain trusts the primary domain to perform operations such as name lookups and authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUST_DIRECTION_OUTBOUND"></a><a id="trust_direction_outbound"></a><dl>
<dt><b>TRUST_DIRECTION_OUTBOUND</b></dt>
</dl>
</td>
<td width="60%">
The primary domain trusts the trusted domain to perform operations such as name lookups and authentication.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUST_DIRECTION_BIDIRECTIONAL"></a><a id="trust_direction_bidirectional"></a><dl>
<dt><b>TRUST_DIRECTION_BIDIRECTIONAL</b></dt>
</dl>
</td>
<td width="60%">
Both domains trust each other.

</td>
</tr>
</table>
 


### -field TrustType

A value that indicates the type of the trust relationship. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUST_TYPE_DOWNLEVEL"></a><a id="trust_type_downlevel"></a><dl>
<dt><b>TRUST_TYPE_DOWNLEVEL</b></dt>
</dl>
</td>
<td width="60%">
The domain controller of the trusted domain is a computer running an operating system earlier than Windows 2000.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUST_TYPE_UPLEVEL"></a><a id="trust_type_uplevel"></a><dl>
<dt><b>TRUST_TYPE_UPLEVEL</b></dt>
</dl>
</td>
<td width="60%">
The domain controller of the Microsoft trusted domain is a computer running Windows 2000 or later.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUST_TYPE_MIT"></a><a id="trust_type_mit"></a><dl>
<dt><b>TRUST_TYPE_MIT</b></dt>
</dl>
</td>
<td width="60%">
The trusted domain is an MIT Kerberos realm.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUST_TYPE_DCE"></a><a id="trust_type_dce"></a><dl>
<dt><b>TRUST_TYPE_DCE</b></dt>
</dl>
</td>
<td width="60%">
The trusted domain is a DCE realm.

</td>
</tr>
<tr>
<td width="40%"><a id="0x5_-_0x000FFFFF"></a><a id="0x5_-_0x000fffff"></a><a id="0X5_-_0X000FFFFF"></a><dl>
<dt><b>0x5 - 0x000FFFFF</b></dt>
</dl>
</td>
<td width="60%">
Reserved for future use.

</td>
</tr>
<tr>
<td width="40%"><a id="0x00100000_to_0xFFF00000"></a><a id="0x00100000_to_0xfff00000"></a><a id="0X00100000_TO_0XFFF00000"></a><dl>
<dt><b>0x00100000 to 0xFFF00000</b></dt>
</dl>
</td>
<td width="60%">
Provider-specific trust levels.

</td>
</tr>
</table>
 


### -field TrustAttributes

A value that indicates the attributes of a trust relationship. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUST_ATTRIBUTE_NON_TRANSITIVE"></a><a id="trust_attribute_non_transitive"></a><dl>
<dt><b>TRUST_ATTRIBUTE_NON_TRANSITIVE</b></dt>
</dl>
</td>
<td width="60%">
Disallow transitivity.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUST_ATTRIBUTE_UPLEVEL_ONLY"></a><a id="trust_attribute_uplevel_only"></a><dl>
<dt><b>TRUST_ATTRIBUTE_UPLEVEL_ONLY</b></dt>
</dl>
</td>
<td width="60%">
The trust link is not valid for client operating systems earlier than Windows 2000.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUST_ATTRIBUTE_FILTER_SIDS"></a><a id="trust_attribute_filter_sids"></a><dl>
<dt><b>TRUST_ATTRIBUTE_FILTER_SIDS</b></dt>
</dl>
</td>
<td width="60%">
Quarantine domains.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUST_ATTRIBUTE_FOREST_TRANSITIVE"></a><a id="trust_attribute_forest_transitive"></a><dl>
<dt><b>TRUST_ATTRIBUTE_FOREST_TRANSITIVE</b></dt>
</dl>
</td>
<td width="60%">
The trust link may contain forest trust information.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUST_ATTRIBUTE_CROSS_ORGANIZATION"></a><a id="trust_attribute_cross_organization"></a><dl>
<dt><b>TRUST_ATTRIBUTE_CROSS_ORGANIZATION</b></dt>
</dl>
</td>
<td width="60%">
This trust is to a domain/forest that is not part of this enterprise.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUST_ATTRIBUTE_TREAT_AS_EXTERNAL"></a><a id="trust_attribute_treat_as_external"></a><dl>
<dt><b>TRUST_ATTRIBUTE_TREAT_AS_EXTERNAL</b></dt>
</dl>
</td>
<td width="60%">
Trust is treated as external for trust boundary purposes.

</td>
</tr>
<tr>
<td width="40%"><a id="TRUST_ATTRIBUTE_WITHIN_FOREST"></a><a id="trust_attribute_within_forest"></a><dl>
<dt><b>TRUST_ATTRIBUTE_WITHIN_FOREST</b></dt>
</dl>
</td>
<td width="60%">
 Trust is internal to this forest.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/9e1cf20f-01f9-4813-bf95-e47c5d57dcdc">LSA_UNICODE_STRING</a>



<a href="https://msdn.microsoft.com/2f458098-9498-4f08-bd13-ac572678d734">LsaCreateTrustedDomainEx</a>



<a href="https://msdn.microsoft.com/62925515-a6f3-4b5f-bf97-edb968af19a3">LsaQueryTrustedDomainInfo</a>



<a href="https://msdn.microsoft.com/d33d6cee-bd8b-49f4-8e65-07cdc65bec7c">LsaQueryTrustedDomainInfoByName</a>



<a href="https://msdn.microsoft.com/263e1025-1010-463d-8bc7-cdf916ce9872">LsaSetTrustedDomainInfoByName</a>



<a href="https://msdn.microsoft.com/442a0944-b498-4d9f-b338-d5aed1663d8d">TRUSTED_INFORMATION_CLASS</a>
 

 

