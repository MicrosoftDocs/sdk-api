---
UID: NF:ntsecapi.LsaSetInformationPolicy
title: LsaSetInformationPolicy function
author: windows-sdk-content
description: Modifies information in a Policy object.
old-location: security\lsasetinformationpolicy.htm
old-project: SecAuthN
ms.assetid: 2aa3b09e-2cd9-4a09-bfd6-b37c97266dcb
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: LsaSetInformationPolicy, LsaSetInformationPolicy function [Security], PolicyAccountDomainInformation, PolicyAuditEventsInformation, PolicyDnsDomainInformation, PolicyLsaServerRoleInformation, PolicyPrimaryDomainInformation, _lsa_lsasetinformationpolicy, ntsecapi/LsaSetInformationPolicy, security.lsasetinformationpolicy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntsecapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TRUSTED_INFORMATION_CLASS, *PTRUSTED_INFORMATION_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-lsapolicy-l1-1-0.dll
 - sechost.dll
 - API-MS-Win-Security-LSAPolicy-L1-1-1.dll
api_name:
 - LsaSetInformationPolicy
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: ADAM
---

# LsaSetInformationPolicy function


## -description


The <b>LsaSetInformationPolicy</b> function modifies information in a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object.


## -parameters




### -param PolicyHandle [in]

A handle to a <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. The required access rights for this handle depend on the value of the <i>InformationClass</i> parameter. For more information, see 
<a href="https://msdn.microsoft.com/66fdc878-d9c4-421c-b79f-9df08984611c">Opening a Policy Object Handle</a>.


### -param InformationClass [in]

Specifies one of the following values from the 
<a href="https://msdn.microsoft.com/b734b5e8-1ee9-436b-b2a9-210ae79fbaf5">POLICY_INFORMATION_CLASS</a> enumeration type. The value indicates the type of information to set. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PolicyAuditEventsInformation"></a><a id="policyauditeventsinformation"></a><a id="POLICYAUDITEVENTSINFORMATION"></a><dl>
<dt><b>PolicyAuditEventsInformation</b></dt>
</dl>
</td>
<td width="60%">
Sets the system's auditing rules. The handle passed in the <i>PolicyHandle</i> parameter must have the POLICY_SET_AUDIT_REQUIREMENTS access right. The <i>Buffer</i> parameter must be a pointer to a 
<a href="https://msdn.microsoft.com/3442e5e5-78cf-4bda-ba11-0f51ee40df16">POLICY_AUDIT_EVENTS_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyPrimaryDomainInformation"></a><a id="policyprimarydomaininformation"></a><a id="POLICYPRIMARYDOMAININFORMATION"></a><dl>
<dt><b>PolicyPrimaryDomainInformation</b></dt>
</dl>
</td>
<td width="60%">
Sets the name and SID of the system's primary domain. The handle passed in the <i>PolicyHandle</i> parameter must have the POLICY_TRUST_ADMIN access right. The <i>Buffer</i> parameter must be a pointer to a 
<a href="https://msdn.microsoft.com/20102da1-bc05-4ea5-9a2d-a50ecba5fd88">POLICY_PRIMARY_DOMAIN_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyAccountDomainInformation"></a><a id="policyaccountdomaininformation"></a><a id="POLICYACCOUNTDOMAININFORMATION"></a><dl>
<dt><b>PolicyAccountDomainInformation</b></dt>
</dl>
</td>
<td width="60%">
Sets the name and SID of the system's account domain. The handle passed in the <i>PolicyHandle</i> parameter must have the POLICY_TRUST_ADMIN access right. The <i>Buffer</i> parameter must be a pointer to a 
<a href="https://msdn.microsoft.com/0e38ac5f-40db-405d-9394-b6bcb7c652b5">POLICY_ACCOUNT_DOMAIN_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyDnsDomainInformation"></a><a id="policydnsdomaininformation"></a><a id="POLICYDNSDOMAININFORMATION"></a><dl>
<dt><b>PolicyDnsDomainInformation</b></dt>
</dl>
</td>
<td width="60%">
Sets Domain Name System (DNS) information about the primary domain associated with the <a href="https://msdn.microsoft.com/4253c7fb-85f5-441d-90bf-492e802ad0f8">Policy</a> object. The handle passed in the <i>PolicyHandle</i> parameter must have the POLICY_TRUST_ADMIN access right. The <i>Buffer</i> parameter must be a pointer to a 
<a href="https://msdn.microsoft.com/5b2879cf-e0dc-4844-bfe8-bf45460285f1">POLICY_DNS_DOMAIN_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="PolicyLsaServerRoleInformation"></a><a id="policylsaserverroleinformation"></a><a id="POLICYLSASERVERROLEINFORMATION"></a><dl>
<dt><b>PolicyLsaServerRoleInformation</b></dt>
</dl>
</td>
<td width="60%">
Sets the role of an LSA server. The handle passed in the <i>PolicyHandle</i> parameter must have the POLICY_SERVER_ADMIN access right. The <i>Buffer</i> parameter must be a pointer to a 
<a href="https://msdn.microsoft.com/f66abe33-d8c8-45b8-9b94-d6890d786aaa">POLICY_LSA_SERVER_ROLE_INFO</a> structure.

Changing a server's role from primary to backup has no effect (although the function returns STATUS_SUCCESS). Changing a server's role from backup to primary requires extensive network operations and may be slow. 

</td>
</tr>
</table>
 


### -param Buffer [in]

Pointer to a structure containing the information to set. The type of structure depends on the value of the <i>InformationClass</i> parameter.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code. For more information, see 
<a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/0e38ac5f-40db-405d-9394-b6bcb7c652b5">POLICY_ACCOUNT_DOMAIN_INFO</a>



<a href="https://msdn.microsoft.com/3442e5e5-78cf-4bda-ba11-0f51ee40df16">POLICY_AUDIT_EVENTS_INFO</a>



<a href="https://msdn.microsoft.com/5b2879cf-e0dc-4844-bfe8-bf45460285f1">POLICY_DNS_DOMAIN_INFO</a>



<a href="https://msdn.microsoft.com/f66abe33-d8c8-45b8-9b94-d6890d786aaa">POLICY_LSA_SERVER_ROLE_INFO</a>



<a href="https://msdn.microsoft.com/20102da1-bc05-4ea5-9a2d-a50ecba5fd88">POLICY_PRIMARY_DOMAIN_INFO</a>
 

 

